pipelineJob(''DSL_Pipeline'') { 
  def repo = ''https://github.com/PriscillaJB19/Node.git'' 
    { 
      scm(''H/5 * * * *'') 
  definition 
  { 
    dependencies{
    def call(Map config = [:]){
      sh "cd ${config.project_root}; npm install"
    }

    }
    build{
      def call (Map config = [:]){
      sh "cd ./${config.project_root};docker build -t ${config.registry}:${config.buildNumber} ."
    }
    }

  } 
}
  
