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



// pipeline {
//     agent any
//     stages {
//         stage('Setup parameters') {
//             steps {
//                 script { 
//                     properties([
//                         parameters([
//                             choice(
//                                 choices: ['ONE', 'TWO'], 
//                                 name: 'PARAMETER_01'
//                             ),
//                             booleanParam(
//                                 defaultValue: true, 
//                                 description: '', 
//                                 name: 'BOOLEAN'
//                             ),
//                             text(
//                                 defaultValue: '''
//                                 this is a multi-line 
//                                 string parameter example
//                                 ''', 
//                                  name: 'MULTI-LINE-STRING'
//                             ),
//                             string(
//                                 defaultValue: 'scriptcrunch', 
//                                 name: 'STRING-PARAMETER', 
//                                 trim: true
//                             )
//                         ])
//                     ])
//                 }
//             }
//         }
//     }   
// }
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
//                                         $class: 'Script', 
//                                         fallbackScript: [
//                                             classpath: [], 
//                                             sandbox: false, 
//                                             script: """
//                                                 return['Could not get The environemnts']
//                                                 """
//                                         ], 
//                                         script: [
//                                             classpath: [], 
//                                             sandbox: false, 
//                                             script: """
//                                                 return['dev','stage','prod']
//                                                 """
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
//                                                 script: '''
//                                                 if (Env.equals("dev")){
//                                                     return["ami-sd2345sd", "ami-asdf245sdf", "ami-asdf3245sd"]
//                                                 }
//                                                 else if(Env.equals("stage")){
//                                                     return["ami-sd34sdf", "ami-sdf345sdc", "ami-sdf34sdf"]
//                                                 }
//                                                 else if(Env.equals("prod")){
//                                                     return["ami-sdf34sdf", "ami-sdf34ds", "ami-sdf3sf3"]
//                                                 }
//                                                 '''
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
//                                             script: '''
//                                                     if (Env.equals("dev")){
//                                                         return["ami-sd2345sd:  AMI with Java", "ami-asdf245sdf: AMI with Python", "ami-asdf3245sd: AMI with Groovy"]
//                                                     }
//                                                     else if(Env.equals("stage")){
//                                                         return["ami-sd34sdf:  AMI with Java", "ami-sdf345sdc: AMI with Python", "ami-sdf34sdf: AMI with Groovy"]
//                                                     }
//                                                     else if(Env.equals("prod")){
//                                                         return["ami-sdf34sdf:  AMI with Java", "ami-sdf34ds: AMI with Python", "ami-sdf3sf3: AMI with Groovy"]
//                                                     }
//                                                     '''
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
// properties([
//   parameters([
//     [
//       $class: 'ChoiceParameter',
//       choiceType: 'PT_SINGLE_SELECT',
//       name: 'Environment',
//       script: [
//         $class: 'ScriptlerScript',
//         scriptlerScriptId:'Environments.groovy'
//       ]
//     ],
//     [
//       $class: 'CascadeChoiceParameter',
//       choiceType: 'PT_SINGLE_SELECT',
//       name: 'Host',
//       referencedParameters: 'Environment',
//       script: [
//         $class: 'ScriptlerScript',
//         scriptlerScriptId:'HostsInEnv.groovy',
//         parameters: [
//           [name:'Environment', value: '$Environment']
//         ]
//       ]
//    ]
//  ])
// ])

// pipeline {
//   agent any
//   parameters {
//     activeChoiceParam('FRUIT', 'Choose your favorite fruit:', ['Apple', 'Banana', 'Cherry'])
//   }
//   stages {
//     stage('Example') {
//       steps {
//         echo "You chose ${params.FRUIT}"
//       }
//     }
//   }
// }


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
//                                                 script: '''
//                                                 if (Env.equals("dev")){
//                                                     return["ami-sd2345sd", "ami-asdf245sdf", "ami-asdf3245sd"]
//                                                 }
//                                                 else if(Env.equals("stage")){
//                                                     return["ami-sd34sdf", "ami-sdf345sdc", "ami-sdf34sdf"]
//                                                 }
//                                                 else if(Env.equals("prod")){
//                                                     return["ami-sdf34sdf", "ami-sdf34ds", "ami-sdf3sf3"]
//                                                 }
//                                                 '''
//                                             ] 
//                                     ]
//                                 ],
//                                 [$class: 'DynamicReferenceParameter', 
//                                     choiceType: 'ET_ORDERED_LIST', 
//                                     description: 'Select the  AMI based on the following information', 
//                                     name: 'Image Information', 
//                                     referencedParameters: 'Env', 
//                                     script: 
//                                         [$class: 'GroovyScript', 
//                                         script: 'return["Could not get AMi Information"]', 
//                                         script: [
//                                             script: '''
//                                                     if (Env.equals("dev")){
//                                                         return["ami-sd2345sd:  AMI with Java", "ami-asdf245sdf: AMI with Python", "ami-asdf3245sd: AMI with Groovy"]
//                                                     }
//                                                     else if(Env.equals("stage")){
//                                                         return["ami-sd34sdf:  AMI with Java", "ami-sdf345sdc: AMI with Python", "ami-sdf34sdf: AMI with Groovy"]
//                                                     }
//                                                     else if(Env.equals("prod")){
//                                                         return["ami-sdf34sdf:  AMI with Java", "ami-sdf34ds: AMI with Python", "ami-sdf3sf3: AMI with Groovy"]
//                                                     }
//                                                     '''
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


// properties([
//   parameters([
//     [
//       $class: 'ChoiceParameter',
//       choiceType: 'PT_SINGLE_SELECT',
//       name: 'Environment',
//       script: [
//         $class: 'ScriptlerScript',
//         scriptlerScriptId:'Environments.groovy'
//       ]
//     ],
//     [
//       $class: 'CascadeChoiceParameter',
//       choiceType: 'PT_SINGLE_SELECT',
//       name: 'Host',
//       referencedParameters: 'Environment',
//       script: [
//         $class: 'ScriptlerScript',
//         scriptlerScriptId:'HostsInEnv.groovy',
//         parameters: [
//           [name:'Environment', value: '$Environment']
//         ]
//       ]
//    ]
//  ])
// ])

// pipeline {
//   agent any
//   stages {
//     stage('Build') {
//       steps {
//         echo "${params.Environment}"
//         echo "${params.Host}"
//       }
//     }
//   }
// }

// import org.jenkinsci.plugins.scriptsecurity.sandbox.groovy.SecureGroovyScript
// import hudson.model.ParametersDefinitionProperty
// import hudson.model.ChoiceParameterDefinition

// def groovyScript = new SecureGroovyScript("""
//     def options = ['Option 1', 'Option 2', 'Option 3']
//     return options
// """, true, null)

// def choiceParam = new ChoiceParameterDefinition(
//     'CHOICE_PARAM',
//     groovyScript,
//     'Choose an option'
// )

// def job = Jenkins.instance.getItemByFullName('my-job-name', Job.class)
// job.addProperty(new ParametersDefinitionProperty(choiceParam))





//final Instance


pipeline {
    agent any
        stages {
            stage('Parameters'){
                steps {
                    script {
                    properties([
                            parameters([
                                [$class: 'ChoiceParameter', 
                                    choiceType: 'PT_SINGLE_SELECT', 
                                    description: 'Select the Environemnt from the Dropdown List', 
                                    filterLength: 1, 
                                    filterable: false, 
                                    name: 'ENVIRONMENT', 
                                    script: [
                                        $class: 'GroovyScript', 
                                        fallbackScript: [
                                            classpath: [], 
                                            sandbox: false, 
                                            script: 
                                                "return['Could not get The environemnts']"
                                        ], 
                                        script: [
                                            classpath: [], 
                                            sandbox: false, 
                                            script: 
                                                "return['ENVIRONMENT_1','ENVIRONMENT_2','ENVIRONMENT_3']"
                                        ]
                                    ]
                                ],
                                [$class: 'CascadeChoiceParameter', 
                                    choiceType: 'PT_SINGLE_SELECT', 
                                    description: 'Select the BUILD ENVIRONMENT from the Dropdown List',
                                    name: 'AMI List', 
                                    referencedParameters: 'ENVIRONMENT', 
                                    script: 
                                        [$class: 'GroovyScript', 
                                        fallbackScript: [
                                                classpath: [], 
                                                sandbox: false, 
                                                script: "return['Could not get Environment from ENVIRONMENT Param']"
                                                ], 
                                        script: [
                                                classpath: [], 
                                                sandbox: false, 
                                                script: '''
                                                if (ENVIRONMENT.equals("ENVIRONMENT_1")){
                                                    return["dev01_01", "preprd01_01", "prd01_01"]
                                                }
                                                else if(ENVIRONMENT.equals("ENVIRONMENT_2")){
                                                    return["dev01_02", "preprd01_02", "prd01_02"]
                                                }
                                                else if(ENVIRONMENT.equals("ENVIRONMENT_3")){
                                                    return["dev01_03", "preprd01_03", "prd01_03"]
                                                }
                                                '''
                                            ] 
                                    ]
                                ],
                                [$class: 'DynamicReferenceParameter', 
                                    choiceType: 'ET_ORDERED_LIST', 
                                    description: 'Select the  AMI based on the following information', 
                                    name: 'Image Information', 
                                    referencedParameters: 'ENVIRONMENT', 
                                    script: 
                                        [$class: 'GroovyScript', 
                                        script: 'return["Could not get AMi Information"]', 
                                        script: [
                                            script: '''
                                                    if (ENVIRONMENT.equals("ENVIRONMENT_1")){
                                                        return["ami-sd2345sd:  AMI with Java", "ami-asdf245sdf: AMI with Python", "ami-asdf3245sd: AMI with Groovy"]
                                                    }
                                                    else if(ENVIRONMENT.equals("ENVIRONMENT_2")){
                                                        return["ami-sd34sdf:  AMI with Java", "ami-sdf345sdc: AMI with Python", "ami-sdf34sdf: AMI with Groovy"]
                                                    }
                                                    else if(ENVIRONMENT.equals("ENVIRONMENT_3")){
                                                        return["ami-sdf34sdf:  AMI with Java", "ami-sdf34ds: AMI with Python", "ami-sdf3sf3: AMI with Groovy"]
                                                    }
                                                    '''
                                                ]
                                        ]
                                ]
                            ])
                        ])
                    }
                }
            }
        }   
}