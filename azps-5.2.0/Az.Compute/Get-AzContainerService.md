---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 23d14e88d7778402d69a6ea3248fa499e5e829cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343925"
---
# <span data-ttu-id="a497c-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a497c-101">Get-AzContainerService</span></span>

## <span data-ttu-id="a497c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a497c-102">SYNOPSIS</span></span>
<span data-ttu-id="a497c-103">Tárolószolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="a497c-103">Gets a container service.</span></span>

## <span data-ttu-id="a497c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="a497c-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a497c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="a497c-105">DESCRIPTION</span></span>
<span data-ttu-id="a497c-106">A **Get-AzContainerService** parancsmag tárolószolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="a497c-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="a497c-107">Megtekintheti a tárolószolgáltatás tulajdonságait, például az állapotot, a főkiszolgáló és az ügynökök számát, valamint a főkiszolgáló és az ügynök teljes tartománynevét.</span><span class="sxs-lookup"><span data-stu-id="a497c-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="a497c-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="a497c-108">EXAMPLES</span></span>

### <span data-ttu-id="a497c-109">1. példa: Tárolószolgáltatás lekérte</span><span class="sxs-lookup"><span data-stu-id="a497c-109">Example 1: Get a container service</span></span>
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

<span data-ttu-id="a497c-110">Ez a parancs egy CSResourceGroup17 nevű tárolószolgáltatást kap.</span><span class="sxs-lookup"><span data-stu-id="a497c-110">This command gets a container service named CSResourceGroup17.</span></span>

### <span data-ttu-id="a497c-111">2. példa: Az összes tárolószolgáltatás lekérte</span><span class="sxs-lookup"><span data-stu-id="a497c-111">Example 2: Get all container services</span></span>
```
PS C:\> Get-AzContainerService

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
ResourceGroup18     CSResourceGroup20   eastus         Succeeded
```

<span data-ttu-id="a497c-112">Ez a parancs az előfizetésben található összes tárolószolgáltatást lekérte.</span><span class="sxs-lookup"><span data-stu-id="a497c-112">This command gets all container services in subscription.</span></span>

### <span data-ttu-id="a497c-113">3. példa: Az összes tárolószolgáltatás lekérte az erőforráscsoportban</span><span class="sxs-lookup"><span data-stu-id="a497c-113">Example 3: Get all container services in resource group</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
```

<span data-ttu-id="a497c-114">Ez a parancs az ResourceGroup17 összes tárolószolgáltatását beveszi.</span><span class="sxs-lookup"><span data-stu-id="a497c-114">This command gets all container services in ResourceGroup17.</span></span>

### <span data-ttu-id="a497c-115">4. példa: Az összes tárolószolgáltatás lekérte a szűrőt</span><span class="sxs-lookup"><span data-stu-id="a497c-115">Example 4: Get all container services using filter</span></span>
```
PS C:\> Get-AzContainerService -Name "CSResourceGroup1*"

ResourceGroupName   Name                Location ProvisioningState
-----------------   ----                -------- -----------------
ResourceGroup17     CSResourceGroup17   eastus         Succeeded
ResourceGroup17     CSResourceGroup18   eastus         Succeeded
ResourceGroup18     CSResourceGroup19   eastus         Succeeded
```

<span data-ttu-id="a497c-116">Ez a parancs az összes tárolószolgáltatást a "CSResourceGroup1" szótól kezdve kapja meg.</span><span class="sxs-lookup"><span data-stu-id="a497c-116">This command gets all container services starting with "CSResourceGroup1".</span></span>

## <span data-ttu-id="a497c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a497c-117">PARAMETERS</span></span>

### <span data-ttu-id="a497c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a497c-118">-DefaultProfile</span></span>
<span data-ttu-id="a497c-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a497c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a497c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a497c-120">-Name</span></span>
<span data-ttu-id="a497c-121">Annak a tárolószolgáltatásnak a nevét adja meg, amelybe a parancsmagot beszerszi.</span><span class="sxs-lookup"><span data-stu-id="a497c-121">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a497c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a497c-122">-ResourceGroupName</span></span>
<span data-ttu-id="a497c-123">Annak a tárolószolgáltatásnak az erőforráscsoportját adja meg, amelybe ez a parancsmag kerül.</span><span class="sxs-lookup"><span data-stu-id="a497c-123">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a497c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a497c-124">CommonParameters</span></span>
<span data-ttu-id="a497c-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a497c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a497c-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a497c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a497c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a497c-127">INPUTS</span></span>

### <span data-ttu-id="a497c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a497c-128">System.String</span></span>

## <span data-ttu-id="a497c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a497c-129">OUTPUTS</span></span>

### <span data-ttu-id="a497c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="a497c-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="a497c-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="a497c-131">NOTES</span></span>

## <span data-ttu-id="a497c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a497c-132">RELATED LINKS</span></span>

[<span data-ttu-id="a497c-133">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a497c-133">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="a497c-134">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a497c-134">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="a497c-135">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="a497c-135">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


