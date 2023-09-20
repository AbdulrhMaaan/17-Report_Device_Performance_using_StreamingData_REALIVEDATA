# 17-Report_Device_Performance_using_StreamingData_REALIVEDATA


#Info About Project
1- Data Source: Stream Data, real-time Data, my Device Performance, Save Data TO SQL DataBase(Local Server)
2- Create Report & Dashboard
3- Cards, Line Card, Table


#Link Of Project

https://app.powerbi.com/view?r=eyJrIjoiZDdmMzMzYmItNmE0ZS00NzgyLWJlNzUtNmFlMDU4ZmE2ZmIzIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9

<iframe title="17-Report_Device_Performance_using_StreamingData_REALIVEDATA" width="600" height="373.5" src="https://app.powerbi.com/view?r=eyJrIjoiZDdmMzMzYmItNmE0ZS00NzgyLWJlNzUtNmFlMDU4ZmE2ZmIzIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9" frameborder="0" allowFullScreen="true"></iframe>


NOTE : cant download the project from powerbi service beacuse the data is real time 


#sQL cODE 
USE [master]
GO
CREATE DATABASE [Monitoring]
GO
USE [Monitoring]
GO
CREATE TABLE [dbo].[Resources](
	[LogDate] [datetime] NULL,
	[DomainName] [nvarchar](30) NULL,
	[ComputerName] [nvarchar](30) NULL,
	[IPAddress] [nvarchar](30) NULL,
	[CPU] [float] NULL,
	[TotalMemory] [float] NULL,
	[FreeMemory] [float] NULL,
	[Memory] [float] NULL,
	[Drives] [nvarchar](max) NULL
)



/****** Script for SelectTopNRows command from SSMS  ******/
SELECT TOP (1000) [LogDate]
      ,[DomainName]
      ,[ComputerName]
      ,[IPAddress]
      ,[CPU]
      ,[TotalMemory]
      ,[FreeMemory]
      ,[Memory]
      ,[Drives]
	  
  FROM [Monitoring].[dbo].[Resources]
