// [
//     $class: 'DynamicReferenceParameter',
//     choiceType: 'ET_FORMATTED_HIDDEN_HTML',
//     name: 'BranchName',
//     omitValueField: true,
//     script: [
//         $class: 'GroovyScript',
//         fallbackScript: [
//             classpath: [],
//             sandbox: true,
//             script: '''
//                 return '<p>error</p>'
//             '''
//         ], 
//         script: [
//             classpath: [],
//             sandbox: true,
//             script: """
//                 return '<input name="value" value="${env.BRANCH_NAME}" type="text">'
//             """
//         ]
//     ]
// ]

// pipeline {
//     parameters {
//         string(name: 'PARAM1', defaultValue: 'default_value', description: 'Description of parameter 1')
//         booleanParam(name: 'PARAM2', defaultValue: true, description: 'Description of parameter 2')
//     }
//     stages {
//         // ...
//         // pipeline {
// //     agent any
// //         stages {
// //             stage('Parameters'){
// //                 steps {
// //                     script {
// //                     properties([
// //                             parameters([
// //                                 [$class: 'ChoiceParameter', 
// //                                     choiceType: 'PT_SINGLE_SELECT', 
// //                                     description: 'Select the Environemnt from the Dropdown List', 
// //                                     filterLength: 1, 
// //                                     filterable: false, 
// //                                     name: 'Env', 
// //                                     script: [
// //                                         $class: 'GroovyScript', 
// //                                         fallbackScript: [
// //                                             classpath: [], 
// //                                             sandbox: false, 
// //                                             script: 
// //                                                 "return['Could not get The environemnts']"
// //                                         ], 
// //                                         script: [
// //                                             classpath: [], 
// //                                             sandbox: false, 
// //                                             script: 
// //                                                 "return['dev','stage','prod']"
// //                                         ]
// //                                     ]
// //                                 ],
// //                                 [$class: 'CascadeChoiceParameter', 
// //                                     choiceType: 'PT_SINGLE_SELECT', 
// //                                     description: 'Select the AMI from the Dropdown List',
// //                                     name: 'AMI List', 
// //                                     referencedParameters: 'Env', 
// //                                     script: 
// //                                         [$class: 'GroovyScript', 
// //                                         fallbackScript: [
// //                                                 classpath: [], 
// //                                                 sandbox: false, 
// //                                                 script: "return['Could not get Environment from Env Param']"
// //                                                 ], 
// //                                         script: [
// //                                                 classpath: [], 
// //                                                 sandbox: false, 
// //                                                 script: '''
// //                                                 if (Env.equals("dev")){
// //                                                     return["ami-sd2345sd", "ami-asdf245sdf", "ami-asdf3245sd"]
// //                                                 }
// //                                                 else if(Env.equals("stage")){
// //                                                     return["ami-sd34sdf", "ami-sdf345sdc", "ami-sdf34sdf"]
// //                                                 }
// //                                                 else if(Env.equals("prod")){
// //                                                     return["ami-sdf34sdf", "ami-sdf34ds", "ami-sdf3sf3"]
// //                                                 }
// //                                                 '''
// //                                             ] 
// //                                     ]
// //                                 ],
// //                                 [$class: 'DynamicReferenceParameter', 
// //                                     choiceType: 'ET_ORDERED_LIST', 
// //                                     description: 'Select the  AMI based on the following infomration', 
// //                                     name: 'Image Information', 
// //                                     referencedParameters: 'Env', 
// //                                     script: 
// //                                         [$class: 'GroovyScript', 
// //                                         script: 'return["Could not get AMi Information"]', 
// //                                         script: [
// //                                             script: '''
// //                                                     if (Env.equals("dev")){
// //                                                         return["ami-sd2345sd:  AMI with Java", "ami-asdf245sdf: AMI with Python", "ami-asdf3245sd: AMI with Groovy"]
// //                                                     }
// //                                                     else if(Env.equals("stage")){
// //                                                         return["ami-sd34sdf:  AMI with Java", "ami-sdf345sdc: AMI with Python", "ami-sdf34sdf: AMI with Groovy"]
// //                                                     }
// //                                                     else if(Env.equals("prod")){
// //                                                         return["ami-sdf34sdf:  AMI with Java", "ami-sdf34ds: AMI with Python", "ami-sdf3sf3: AMI with Groovy"]
// //                                                     }
// //                                                     '''
// //                                                 ]
// //                                         ]
// //                                 ]
// //                             ])
// //                         ])
// //                     }
// //                 }
// //             }
// //         }   
// // }
//     }
// }



pipeline {
    agent any
    stages {
        stage('Setup parameters') {
            steps {
                script { 
                    properties([
                        parameters([
                            choice(
                                choices: ['ONE', 'TWO'], 
                                name: 'PARAMETER_01'
                            ),
                            booleanParam(
                                defaultValue: true, 
                                description: '', 
                                name: 'BOOLEAN'
                            ),
                            text(
                                defaultValue: '''
                                this is a multi-line 
                                string parameter example
                                ''', 
                                 name: 'MULTI-LINE-STRING'
                            ),
                            string(
                                defaultValue: 'scriptcrunch', 
                                name: 'STRING-PARAMETER', 
                                trim: true
                            )
                        ])
                    ])
                }
            }
        }
    }   
}
// pipeline {
//     agent any
//         stages {
//             stage('Parameters'){
//                 steps {
//                     script {
//                     properties([
//                             parameters([
//                                 [$class: 'ChoiceParameter', 
//                                     choiceType: 'PT_SINGLE_SELECT', 
//                                     description: 'Select the Environemnt from the Dropdown List', 
//                                     filterLength: 1, 
//                                     filterable: false, 
//                                     name: 'Env', 
//                                     script: [
//                                         $class: 'GroovyScript', 
//                                         fallbackScript: [
//                                             classpath: [], 
//                                             sandbox: false, 
//                                             script: 
//                                                 "return['Could not get The environemnts']"
//                                         ], 
//                                         script: [
//                                             classpath: [], 
//                                             sandbox: false, 
//                                             script: 
//                                                 "return['dev','stage','prod']"
//                                         ]
//                                     ]
//                                 ],
//                                 [$class: 'CascadeChoiceParameter', 
//                                     choiceType: 'PT_SINGLE_SELECT', 
//                                     description: 'Select the AMI from the Dropdown List',
//                                     name: 'AMI List', 
//                                     referencedParameters: 'Env', 
//                                     script: 
//                                         [$class: 'GroovyScript', 
//                                         fallbackScript: [
//                                                 classpath: [], 
//                                                 sandbox: false, 
//                                                 script: "return['Could not get Environment from Env Param']"
//                                                 ], 
//                                         script: [
//                                                 classpath: [], 
//                                                 sandbox: false, 
//                                                 script:
//                                                 if (Env.equals("dev")){
//                                                     return["ami-sd2345sd", "ami-asdf245sdf", "ami-asdf3245sd"]
//                                                 }
//                                                 else if(Env.equals("stage")){
//                                                     return["ami-sd34sdf", "ami-sdf345sdc", "ami-sdf34sdf"]
//                                                 }
//                                                 else if(Env.equals("prod")){
//                                                     return["ami-sdf34sdf", "ami-sdf34ds", "ami-sdf3sf3"]
//                                                 }
//                                             ] 
//                                     ]
//                                 ],
//                                 [$class: 'DynamicReferenceParameter', 
//                                     choiceType: 'ET_ORDERED_LIST', 
//                                     description: 'Select the  AMI based on the following infomration', 
//                                     name: 'Image Information', 
//                                     referencedParameters: 'Env', 
//                                     script: 
//                                         [$class: 'GroovyScript', 
//                                         script: 'return["Could not get AMi Information"]', 
//                                         script: [
//                                             script: 
//                                                     if (Env.equals("dev")){
//                                                         return["ami-sd2345sd:  AMI with Java", "ami-asdf245sdf: AMI with Python", "ami-asdf3245sd: AMI with Groovy"]
//                                                     }
//                                                     else if(Env.equals("stage")){
//                                                         return["ami-sd34sdf:  AMI with Java", "ami-sdf345sdc: AMI with Python", "ami-sdf34sdf: AMI with Groovy"]
//                                                     }
//                                                     else if(Env.equals("prod")){
//                                                         return["ami-sdf34sdf:  AMI with Java", "ami-sdf34ds: AMI with Python", "ami-sdf3sf3: AMI with Groovy"]
//                                                     }
//                                                 ]
//                                         ]
//                                 ]
//                             ])
//                         ])
//                     }
//                 }
//             }
//         }   
// }