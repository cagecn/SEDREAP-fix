# SEDREAP-fix
fix SEDREAP svg unvisible on ie11 firefox chrome

1.Add these lines to C:\Program Files\SEDREAP\Resources\Sdr\WEB-INF\web.xml

	<filter>
		<filter-name>GzipHeaderFilter</filter-name>
		<filter-class>ht.cage.sdr.fix.filter.SvgLoaderFilter</filter-class>
	</filter>
	<filter-mapping>
		<filter-name>GzipHeaderFilter</filter-name>
		<url-pattern>/svgLoader</url-pattern>
	</filter-mapping>
after


	<filter-mapping>
		<filter-name>sessiontimeoutfilter</filter-name>
		<servlet-name>svgLoader</servlet-name>
	</filter-mapping>
  
  
2.put SEDREAP-fix.jar to C:\Program Files\SEDREAP\Resources\Sdr\WEB-INF\lib

3.restart SEDREAP，then you will watch svg formate print


cage.Lau@qq.com
