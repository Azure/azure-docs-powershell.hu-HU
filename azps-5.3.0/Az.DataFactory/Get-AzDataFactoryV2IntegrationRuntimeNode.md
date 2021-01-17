---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4d99a495863f93acfb97b290488fd0db24d69444
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480430"
---
# <span data-ttu-id="1d651-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1d651-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="1d651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d651-102">SYNOPSIS</span></span>
<span data-ttu-id="1d651-103">Integrációs futásidejű csomópontadatokat kap.</span><span class="sxs-lookup"><span data-stu-id="1d651-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="1d651-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="1d651-104">SYNTAX</span></span>

### <span data-ttu-id="1d651-105">ByIntegrationRuntimeName (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d651-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1d651-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d651-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d651-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="1d651-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d651-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="1d651-108">DESCRIPTION</span></span>
<span data-ttu-id="1d651-109">A **Get-AzDataFactoryV2IntegrationRuntimeNode** parancsmag megkapja az integrációs futásidejű csomópont részletes adatait.</span><span class="sxs-lookup"><span data-stu-id="1d651-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="1d651-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="1d651-110">EXAMPLES</span></span>

### <span data-ttu-id="1d651-111">1. példa: Egy integrációs futásidejű csomópont részletes adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="1d651-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
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

<span data-ttu-id="1d651-112">A parancsmag a "test-df-eu2" data factory "test-df-eu2" nevű, önkiszolgáló integrációs futásidejű "test-selfhost-ir" "Node_1" nevű csomópontról kap információkat.</span><span class="sxs-lookup"><span data-stu-id="1d651-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="1d651-113">2. példa: Egy integrációs futásidejű csomópont részletes adatait az IP-címmel együtt kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1d651-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
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

<span data-ttu-id="1d651-114">A parancsmag információkat kap a "test-df-eu2" data factory "test-df-eu2" nevű, önkiszolgáló integrációs futásidejű "test-selfhost-ir" "Node_1" nevű csomópontról, beleértve az IP-címet is.</span><span class="sxs-lookup"><span data-stu-id="1d651-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="1d651-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d651-115">PARAMETERS</span></span>

### <span data-ttu-id="1d651-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1d651-116">-DataFactoryName</span></span>
<span data-ttu-id="1d651-117">Az adatüzem neve.</span><span class="sxs-lookup"><span data-stu-id="1d651-117">The data factory name.</span></span>

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

### <span data-ttu-id="1d651-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d651-118">-DefaultProfile</span></span>
<span data-ttu-id="1d651-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d651-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d651-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d651-120">-InputObject</span></span>
<span data-ttu-id="1d651-121">Az integráció futásidejű objektuma.</span><span class="sxs-lookup"><span data-stu-id="1d651-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="1d651-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="1d651-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="1d651-123">Az integráció futásidejű neve.</span><span class="sxs-lookup"><span data-stu-id="1d651-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="1d651-124">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="1d651-124">-IpAddress</span></span>
<span data-ttu-id="1d651-125">Az integrációs futásidejű csomópont IP-címe.</span><span class="sxs-lookup"><span data-stu-id="1d651-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="1d651-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1d651-126">-Name</span></span>
<span data-ttu-id="1d651-127">Az integráció futásidejű csomópontjának neve.</span><span class="sxs-lookup"><span data-stu-id="1d651-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="1d651-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d651-128">-ResourceGroupName</span></span>
<span data-ttu-id="1d651-129">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1d651-129">The resource group name.</span></span>

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

### <span data-ttu-id="1d651-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d651-130">-ResourceId</span></span>
<span data-ttu-id="1d651-131">Az Azure-erőforrásazonosító.</span><span class="sxs-lookup"><span data-stu-id="1d651-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1d651-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d651-132">CommonParameters</span></span>
<span data-ttu-id="1d651-133">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d651-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d651-134">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d651-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d651-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1d651-135">INPUTS</span></span>

### <span data-ttu-id="1d651-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1d651-136">System.String</span></span>

### <span data-ttu-id="1d651-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1d651-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="1d651-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d651-138">OUTPUTS</span></span>

### <span data-ttu-id="1d651-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1d651-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="1d651-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="1d651-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="1d651-141">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="1d651-141">NOTES</span></span>
<span data-ttu-id="1d651-142">Kulcsszavak: azure, azurerm, arm, erőforrás, kezelés, kezelő, adatok, faktorok, másolás, tevékenységek, integráció futásideje</span><span class="sxs-lookup"><span data-stu-id="1d651-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="1d651-143">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d651-143">RELATED LINKS</span></span>

[<span data-ttu-id="1d651-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="1d651-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()
