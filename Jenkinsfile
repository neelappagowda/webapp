pipeline {
	agent none
	stages {
	stage ( 'c-project and java' ) {
		parallel {
		stage ('make') {
			agent { label 'c-node' }
			steps {
			  	git 'https://github.com/neelappagowda/c-project_1.git'
					sh 'make'
				echo 'This is slaveforc node with STAGE 1'
						sh 'sleep 10'
			}
		}
		stage ('Java Project') {
			agent { label 'java-node' }
			 tools {
        maven 'Apache Maven 3.0.5' 
    }
			steps {
				 sh '''
				 java.lang.IllegalArgumentException: /usr/bin/mvn
	at org.jenkinsci.plugins.workflow.steps.EnvStep.<init>(EnvStep.java:52)
	at org.jenkinsci.plugins.workflow.steps.EnvStep$DescriptorImpl.newInstance(EnvStep.java:130)
	at org.jenkinsci.plugins.workflow.steps.EnvStep$DescriptorImpl.newInstance(EnvStep.java:106)
	at org.jenkinsci.plugins.workflow.cps.Snippetizer.doGenerateSnippet(Snippetizer.java:502)
	at java.lang.invoke.MethodHandle.invokeWithArguments(MethodHandle.java:627)
	at org.kohsuke.stapler.Function$MethodFunction.invoke(Function.java:396)
	at org.kohsuke.stapler.Function$InstanceFunction.invoke(Function.java:408)
	at org.kohsuke.stapler.Function.bindAndInvoke(Function.java:212)
	at org.kohsuke.stapler.Function.bindAndInvokeAndServeResponse(Function.java:145)
	at org.kohsuke.stapler.MetaClass$11.doDispatch(MetaClass.java:536)
	at org.kohsuke.stapler.NameBasedDispatcher.dispatch(NameBasedDispatcher.java:58)
	at org.kohsuke.stapler.Stapler.tryInvoke(Stapler.java:766)
	at org.kohsuke.stapler.Stapler.invoke(Stapler.java:898)
	at org.kohsuke.stapler.MetaClass$9.dispatch(MetaClass.java:457)
	at org.kohsuke.stapler.Stapler.tryInvoke(Stapler.java:766)
	at org.kohsuke.stapler.Stapler.invoke(Stapler.java:898)
	at org.kohsuke.stapler.Stapler.invoke(Stapler.java:694)
	at org.kohsuke.stapler.Stapler.service(Stapler.java:240)
	at javax.servlet.http.HttpServlet.service(HttpServlet.java:790)
	at org.eclipse.jetty.servlet.ServletHolder.handle(ServletHolder.java:763)
	at org.eclipse.jetty.servlet.ServletHandler$CachedChain.doFilter(ServletHandler.java:1631)
	at hudson.util.PluginServletFilter$1.doFilter(PluginServletFilter.java:154)
	at org.jenkinsci.plugins.ssegateway.Endpoint$SSEListenChannelFilter.doFilter(Endpoint.java:248)
	at hudson.util.PluginServletFilter$1.doFilter(PluginServletFilter.java:151)
	at jenkins.security.ResourceDomainFilter.doFilter(ResourceDomainFilter.java:76)
	at hudson.util.PluginServletFilter$1.doFilter(PluginServletFilter.java:151)
	at jenkins.telemetry.impl.UserLanguages$AcceptLanguageFilter.doFilter(UserLanguages.java:129)
	at hudson.util.PluginServletFilter$1.doFilter(PluginServletFilter.java:151)
	at io.jenkins.blueocean.ResourceCacheControl.doFilter(ResourceCacheControl.java:134)
	at hudson.util.PluginServletFilter$1.doFilter(PluginServletFilter.java:151)
	at io.jenkins.blueocean.auth.jwt.impl.JwtAuthenticationFilter.doFilter(JwtAuthenticationFilter.java:60)
	at hudson.util.PluginServletFilter$1.doFilter(PluginServletFilter.java:151)
	at hudson.util.PluginServletFilter.doFilter(PluginServletFilter.java:157)
	at org.eclipse.jetty.servlet.ServletHandler$CachedChain.doFilter(ServletHandler.java:1618)
	at hudson.security.csrf.CrumbFilter.doFilter(CrumbFilter.java:153)
	at org.eclipse.jetty.servlet.ServletHandler$CachedChain.doFilter(ServletHandler.java:1618)
	at hudson.security.ChainedServletFilter$1.doFilter(ChainedServletFilter.java:84)
	at hudson.security.UnwrapSecurityExceptionFilter.doFilter(UnwrapSecurityExceptionFilter.java:51)
	at hudson.security.ChainedServletFilter$1.doFilter(ChainedServletFilter.java:87)
	at jenkins.security.ExceptionTranslationFilter.doFilter(ExceptionTranslationFilter.java:119)
	at hudson.security.ChainedServletFilter$1.doFilter(ChainedServletFilter.java:87)
	at org.acegisecurity.providers.anonymous.AnonymousProcessingFilter.doFilter(AnonymousProcessingFilter.java:125)
	at hudson.security.ChainedServletFilter$1.doFilter(ChainedServletFilter.java:87)
	at org.acegisecurity.ui.rememberme.RememberMeProcessingFilter.doFilter(RememberMeProcessingFilter.java:142)
	at hudson.security.ChainedServletFilter$1.doFilter(ChainedServletFilter.java:87)
	at org.acegisecurity.ui.AbstractProcessingFilter.doFilter(AbstractProcessingFilter.java:271)
	at hudson.security.ChainedServletFilter$1.doFilter(ChainedServletFilter.java:87)
	at jenkins.security.BasicHeaderProcessor.doFilter(BasicHeaderProcessor.java:93)
	at hudson.security.ChainedServletFilter$1.doFilter(ChainedServletFilter.java:87)
	at org.acegisecurity.context.HttpSessionContextIntegrationFilter.doFilter(HttpSessionContextIntegrationFilter.java:249)
	at hudson.security.HttpSessionContextIntegrationFilter2.doFilter(HttpSessionContextIntegrationFilter2.java:67)
	at hudson.security.ChainedServletFilter$1.doFilter(ChainedServletFilter.java:87)
	at hudson.security.ChainedServletFilter.doFilter(ChainedServletFilter.java:90)
	at hudson.security.HudsonFilter.doFilter(HudsonFilter.java:171)
	at org.eclipse.jetty.servlet.ServletHandler$CachedChain.doFilter(ServletHandler.java:1618)
	at org.kohsuke.stapler.compression.CompressionFilter.doFilter(CompressionFilter.java:51)
	at org.eclipse.jetty.servlet.ServletHandler$CachedChain.doFilter(ServletHandler.java:1618)
	at hudson.util.CharacterEncodingFilter.doFilter(CharacterEncodingFilter.java:82)
	at org.eclipse.jetty.servlet.ServletHandler$CachedChain.doFilter(ServletHandler.java:1618)
	at org.kohsuke.stapler.DiagnosticThreadNameFilter.doFilter(DiagnosticThreadNameFilter.java:30)
	at org.eclipse.jetty.servlet.ServletHandler$CachedChain.doFilter(ServletHandler.java:1618)
	at jenkins.security.SuspiciousRequestFilter.doFilter(SuspiciousRequestFilter.java:36)
	at org.eclipse.jetty.servlet.ServletHandler$CachedChain.doFilter(ServletHandler.java:1618)
	at org.eclipse.jetty.servlet.ServletHandler.doHandle(ServletHandler.java:549)
	at org.eclipse.jetty.server.handler.ScopedHandler.handle(ScopedHandler.java:143)
	at org.eclipse.jetty.security.SecurityHandler.handle(SecurityHandler.java:578)
	at org.eclipse.jetty.server.handler.HandlerWrapper.handle(HandlerWrapper.java:127)
	at org.eclipse.jetty.server.handler.ScopedHandler.nextHandle(ScopedHandler.java:235)
	at org.eclipse.jetty.server.session.SessionHandler.doHandle(SessionHandler.java:1610)
	at org.eclipse.jetty.server.handler.ScopedHandler.nextHandle(ScopedHandler.java:233)
	at org.eclipse.jetty.server.handler.ContextHandler.doHandle(ContextHandler.java:1369)
	at org.eclipse.jetty.server.handler.ScopedHandler.nextScope(ScopedHandler.java:188)
	at org.eclipse.jetty.servlet.ServletHandler.doScope(ServletHandler.java:489)
	at org.eclipse.jetty.server.session.SessionHandler.doScope(SessionHandler.java:1580)
	at org.eclipse.jetty.server.handler.ScopedHandler.nextScope(ScopedHandler.java:186)
	at org.eclipse.jetty.server.handler.ContextHandler.doScope(ContextHandler.java:1284)
	at org.eclipse.jetty.server.handler.ScopedHandler.handle(ScopedHandler.java:141)
	at org.eclipse.jetty.server.handler.HandlerWrapper.handle(HandlerWrapper.java:127)
	at org.eclipse.jetty.server.Server.handle(Server.java:501)
	at org.eclipse.jetty.server.HttpChannel.lambda$handle$1(HttpChannel.java:383)
	at org.eclipse.jetty.server.HttpChannel.dispatch(HttpChannel.java:556)
	at org.eclipse.jetty.server.HttpChannel.handle(HttpChannel.java:375)
	at org.eclipse.jetty.server.HttpConnection.onFillable(HttpConnection.java:272)
	at org.eclipse.jetty.io.AbstractConnection$ReadCallback.succeeded(AbstractConnection.java:311)
	at org.eclipse.jetty.io.FillInterest.fillable(FillInterest.java:103)
	at org.eclipse.jetty.io.ChannelEndPoint$1.run(ChannelEndPoint.java:104)
	at org.eclipse.jetty.util.thread.strategy.EatWhatYouKill.runTask(EatWhatYouKill.java:336)
	at org.eclipse.jetty.util.thread.strategy.EatWhatYouKill.doProduce(EatWhatYouKill.java:313)
	at org.eclipse.jetty.util.thread.strategy.EatWhatYouKill.tryProduce(EatWhatYouKill.java:171)
	at org.eclipse.jetty.util.thread.strategy.EatWhatYouKill.run(EatWhatYouKill.java:129)
	at org.eclipse.jetty.util.thread.ReservedThreadExecutor$ReservedThread.run(ReservedThreadExecutor.java:375)
	at org.eclipse.jetty.util.thread.QueuedThreadPool.runJob(QueuedThreadPool.java:806)
	at org.eclipse.jetty.util.thread.QueuedThreadPool$Runner.run(QueuedThreadPool.java:938)
	at java.lang.Thread.run(Thread.java:748)
				 mvn --version
				git 'https://github.com/neelappagowda/Test.git'
				mvn clean install
				'''
			}
		}
		}
	}
		
	}
}
