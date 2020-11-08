---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 23d14e88d7778402d69a6ea3248fa499e5e829cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94013441"
---
# <span data-ttu-id="cd3fe-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="cd3fe-101">Get-AzContainerService</span></span>

## <span data-ttu-id="cd3fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="cd3fe-103">Tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-103">Gets a container service.</span></span>

## <span data-ttu-id="cd3fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd3fe-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd3fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd3fe-105">DESCRIPTION</span></span>
<span data-ttu-id="cd3fe-106">A **Get-AzContainerService** parancsmag tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="cd3fe-107">Megtekintheti a tároló szolgáltatás tulajdonságait, amely tartalmazza az állapotot, a mesteralakzatok számát és az ügynököket, valamint a mesteralakzat és az ügynök teljes tartománynevét is.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="cd3fe-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cd3fe-108">EXAMPLES</span></span>

### <span data-ttu-id="cd3fe-109">Példa 1: tároló szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="cd3fe-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"

ResourceGroupName     : ResourceGroup17
ProvisioningState     : Succeeded
OrchestratorProfile   :
  OrchestratorType    : DCOS
MasterProfile         :
  Count               : 1
  DnsPrefix           : MasterResourceGroup17
  Fqdn                : masterresourcegroup17.eastus.cloudapp.azure.com
AgentPoolProfiles[0]  :
  Name                : AgentPool01
  Count               : 2
  VmSize              : Standard_A1
  DnsPrefix           : APResourceGroup17
  Fqdn                : apresourcegroup17.eastus.cloudapp.azure.com
LinuxProfile          :
  AdminUsername       : acslinuxadmin
  Ssh                 :
    PublicKeys[0]     :
      KeyData         : ssh-rsa xxxxxxxxxxxxxx contoso@microsoft.com
DiagnosticsProfile    :
  VmDiagnostics       :
    Enabled           : False
    StorageUri        : https://xxxxxxxxxxx.blob.core.windows.net/
Id                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup17/providers/Micr
osoft.ContainerService/containerServices/CSResourceGroup17
Name                  : CSResourceGroup17
Type                  : Microsoft.ContainerService/ContainerServices
Location              : eastus
Tags                  : {}
```

<span data-ttu-id="cd3fe-110">Ez a parancs CSResourceGroup17 nevű tároló szolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="cd3fe-111">2. példa: az összes tároló szolgáltatás beszerzése</span><span class="sxs-lookup"><span data-stu-id="cd3fe-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="cd3fe-112">Ez a parancs beilleszti az előfizetésben az összes tároló szolgáltatást.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="cd3fe-113">3. példa: az összes tároló szolgáltatás beolvasása az erőforrás csoportban</span><span class="sxs-lookup"><span data-stu-id="cd3fe-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="cd3fe-114">Ez a parancs a ResourceGroup17 minden tároló szolgáltatását bekapja.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="cd3fe-115">Példa 4: az összes tároló szolgáltatás beszerzése szűrő használatával</span><span class="sxs-lookup"><span data-stu-id="cd3fe-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="cd3fe-116">Ez a parancs a "CSResourceGroup1" kezdetű összes tároló szolgáltatást megkapja.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="cd3fe-117">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd3fe-117">PARAMETERS</span></span>

### <span data-ttu-id="cd3fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd3fe-118">-DefaultProfile</span></span>
<span data-ttu-id="cd3fe-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd3fe-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd3fe-120">-Name</span></span>
<span data-ttu-id="cd3fe-121">Annak a tároló szolgáltatásnak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-121">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cd3fe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd3fe-122">-ResourceGroupName</span></span>
<span data-ttu-id="cd3fe-123">Annak a tároló szolgáltatásnak az erőforrás csoportját adja meg, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cd3fe-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd3fe-124">CommonParameters</span></span>
<span data-ttu-id="cd3fe-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd3fe-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd3fe-126">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cd3fe-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd3fe-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd3fe-127">INPUTS</span></span>

### <span data-ttu-id="cd3fe-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cd3fe-128">System.String</span></span>

## <span data-ttu-id="cd3fe-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd3fe-129">OUTPUTS</span></span>

### <span data-ttu-id="cd3fe-130">Microsoft. Azure. commands. számítási. Automation. models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="cd3fe-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="cd3fe-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd3fe-131">NOTES</span></span>

## <span data-ttu-id="cd3fe-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd3fe-132">RELATED LINKS</span></span>

[<span data-ttu-id="cd3fe-133">Új – AzContainerService</span><span class="sxs-lookup"><span data-stu-id="cd3fe-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="cd3fe-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="cd3fe-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="cd3fe-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="cd3fe-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


