---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4da5387d5506733ff5046fc34f43bcc003c2b8be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836525"
---
# <span data-ttu-id="8fa70-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8fa70-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="8fa70-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8fa70-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa70-103">Beolvassa az integrációs futtatókörnyezet csomópontjának adatait.</span><span class="sxs-lookup"><span data-stu-id="8fa70-103">Gets an integration runtime node infomation.</span></span>

## <span data-ttu-id="8fa70-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8fa70-104">SYNTAX</span></span>

### <span data-ttu-id="8fa70-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8fa70-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fa70-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8fa70-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fa70-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8fa70-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fa70-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="8fa70-108">DESCRIPTION</span></span>
<span data-ttu-id="8fa70-109">A **Get-AzDataFactoryV2IntegrationRuntimeNode** parancsmag az integrációs futásidejű csomópontok részletes adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8fa70-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="8fa70-110">Példák</span><span class="sxs-lookup"><span data-stu-id="8fa70-110">EXAMPLES</span></span>

### <span data-ttu-id="8fa70-111">Példa 1: az integrációs futtatókörnyezet csomópontjának részletes adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8fa70-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="8fa70-112">A parancsmag az "Node_1" nevű csomópontról ad információt az "ellenőrzés – selfhost – IR" "teszt-DF-EU2" adatkezelési futtatókörnyezetben.</span><span class="sxs-lookup"><span data-stu-id="8fa70-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="8fa70-113">2. példa: az integrációs futtatókörnyezet csomópontjának részletes adatait az IP-címmel együtt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8fa70-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="8fa70-114">A parancsmag az "Node_1" nevű csomópontról ad információt az "ellenőrzés – selfhost – IR" "teszt-DF-EU2" adatkezelési futtatókörnyezetben, az IP-címmel együtt.</span><span class="sxs-lookup"><span data-stu-id="8fa70-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="8fa70-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8fa70-115">PARAMETERS</span></span>

### <span data-ttu-id="8fa70-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8fa70-116">-DataFactoryName</span></span>
<span data-ttu-id="8fa70-117">Az adatgyári név.</span><span class="sxs-lookup"><span data-stu-id="8fa70-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa70-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa70-118">-DefaultProfile</span></span>
<span data-ttu-id="8fa70-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8fa70-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa70-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8fa70-120">-InputObject</span></span>
<span data-ttu-id="8fa70-121">Az integrációs futtatókörnyezet objektuma.</span><span class="sxs-lookup"><span data-stu-id="8fa70-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa70-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="8fa70-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="8fa70-123">Az integrációs futásidejű név.</span><span class="sxs-lookup"><span data-stu-id="8fa70-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa70-124">-Ip_cím</span><span class="sxs-lookup"><span data-stu-id="8fa70-124">-IpAddress</span></span>
<span data-ttu-id="8fa70-125">Az integrációs futásidejű csomópont IP-címe.</span><span class="sxs-lookup"><span data-stu-id="8fa70-125">The IP Address of integration runtime node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa70-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8fa70-126">-Name</span></span>
<span data-ttu-id="8fa70-127">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="8fa70-127">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8fa70-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fa70-128">-ResourceGroupName</span></span>
<span data-ttu-id="8fa70-129">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="8fa70-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa70-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fa70-130">-ResourceId</span></span>
<span data-ttu-id="8fa70-131">Az Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="8fa70-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fa70-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa70-132">CommonParameters</span></span>
<span data-ttu-id="8fa70-133">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8fa70-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa70-134">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa70-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa70-135">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fa70-135">INPUTS</span></span>

### <span data-ttu-id="8fa70-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8fa70-136">System.String</span></span>

### <span data-ttu-id="8fa70-137">Microsoft. Azure. Command. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8fa70-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8fa70-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8fa70-138">OUTPUTS</span></span>

### <span data-ttu-id="8fa70-139">Microsoft. Azure. Command. DataFactoryV2. models. PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8fa70-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="8fa70-140">Microsoft. Azure. Command. DataFactoryV2. models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="8fa70-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="8fa70-141">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8fa70-141">NOTES</span></span>
<span data-ttu-id="8fa70-142">Kulcsszavak: Azure, azurerm, ARM, erőforrás, kezelés, vezető, Data, gyárak, másolás, tevékenységek, integrációs futtatókörnyezet</span><span class="sxs-lookup"><span data-stu-id="8fa70-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="8fa70-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8fa70-143">RELATED LINKS</span></span>

[<span data-ttu-id="8fa70-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8fa70-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
