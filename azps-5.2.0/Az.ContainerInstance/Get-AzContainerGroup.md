---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 2dadcac9f0b537a52a0a7270b7d20fc08e80461c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351222"
---
# <span data-ttu-id="03504-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="03504-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="03504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03504-102">SYNOPSIS</span></span>
<span data-ttu-id="03504-103">Tárolócsoportokat kap.</span><span class="sxs-lookup"><span data-stu-id="03504-103">Gets container groups.</span></span>

## <span data-ttu-id="03504-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="03504-104">SYNTAX</span></span>

### <span data-ttu-id="03504-105">ListContainerGroupParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03504-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03504-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="03504-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03504-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="03504-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03504-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="03504-108">DESCRIPTION</span></span>
<span data-ttu-id="03504-109">A **Get-AzContainerGroup** parancsmag egy adott tárolócsoportot vagy egy erőforráscsoport vagy az előfizetés összes tárolócsoportját megkapja.</span><span class="sxs-lookup"><span data-stu-id="03504-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="03504-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="03504-110">EXAMPLES</span></span>

### <span data-ttu-id="03504-111">1. példa: Egy megadott tárolócsoportot kap</span><span class="sxs-lookup"><span data-stu-id="03504-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="03504-112">A parancs a megadott tárolócsoportot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="03504-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="03504-113">2. példa: Tárolócsoportok lekérte egy erőforráscsoportba</span><span class="sxs-lookup"><span data-stu-id="03504-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="03504-114">A parancs az erőforráscsoport tárolócsoportját kapja `demo` meg.</span><span class="sxs-lookup"><span data-stu-id="03504-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="03504-115">3. példa: Tárolócsoportok lekérte az aktuális előfizetésben</span><span class="sxs-lookup"><span data-stu-id="03504-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="03504-116">A parancs az aktuális előfizetés tárolócsoportját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="03504-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="03504-117">4. példa: Tárolócsoportokat kap erőforrás-azonosító használatával.</span><span class="sxs-lookup"><span data-stu-id="03504-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="03504-118">A parancs lekérte a tárolócsoportot az erőforrás-azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="03504-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="03504-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03504-119">PARAMETERS</span></span>

### <span data-ttu-id="03504-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03504-120">-DefaultProfile</span></span>
<span data-ttu-id="03504-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03504-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03504-122">-Name</span><span class="sxs-lookup"><span data-stu-id="03504-122">-Name</span></span>
<span data-ttu-id="03504-123">A tárolócsoport Neve.</span><span class="sxs-lookup"><span data-stu-id="03504-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03504-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03504-124">-ResourceGroupName</span></span>
<span data-ttu-id="03504-125">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="03504-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03504-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03504-126">-ResourceId</span></span>
<span data-ttu-id="03504-127">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="03504-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03504-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03504-128">CommonParameters</span></span>
<span data-ttu-id="03504-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03504-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03504-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03504-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03504-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03504-131">INPUTS</span></span>

### <span data-ttu-id="03504-132">System.String</span><span class="sxs-lookup"><span data-stu-id="03504-132">System.String</span></span>

## <span data-ttu-id="03504-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03504-133">OUTPUTS</span></span>

### <span data-ttu-id="03504-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="03504-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="03504-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="03504-135">NOTES</span></span>

## <span data-ttu-id="03504-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03504-136">RELATED LINKS</span></span>
