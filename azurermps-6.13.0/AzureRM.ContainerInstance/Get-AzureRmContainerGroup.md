---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/get-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerGroup.md
ms.openlocfilehash: b2107a667fe3d00ec0b6e9180b2edc99e864445c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491978"
---
# <span data-ttu-id="c69e3-101">Get-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c69e3-101">Get-AzureRmContainerGroup</span></span>

## <span data-ttu-id="c69e3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c69e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c69e3-103">Tároló csoportokba kerül.</span><span class="sxs-lookup"><span data-stu-id="c69e3-103">Gets container groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c69e3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c69e3-104">SYNTAX</span></span>

### <span data-ttu-id="c69e3-105">ListContainerGroupParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c69e3-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzureRmContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c69e3-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="c69e3-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c69e3-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="c69e3-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzureRmContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c69e3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="c69e3-108">DESCRIPTION</span></span>
<span data-ttu-id="c69e3-109">A **Get-AzureRmContainerGroup** parancsmag a megadott tároló vagy az erőforráscsoport összes tároló csoportját, illetve az előfizetést kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c69e3-109">The **Get-AzureRmContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="c69e3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="c69e3-110">EXAMPLES</span></span>

### <span data-ttu-id="c69e3-111">Példa 1: a megadott tároló csoport beolvasása</span><span class="sxs-lookup"><span data-stu-id="c69e3-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer

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

<span data-ttu-id="c69e3-112">A parancs a megadott tároló csoportba kerül.</span><span class="sxs-lookup"><span data-stu-id="c69e3-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="c69e3-113">2. példa: egy erőforráscsoport tároló csoportjának beolvasása</span><span class="sxs-lookup"><span data-stu-id="c69e3-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="c69e3-114">A parancs a tároló csoportokat az erőforrás csoportban kapja `demo` .</span><span class="sxs-lookup"><span data-stu-id="c69e3-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="c69e3-115">3. példa: a Container-csoportok bekerülnek az aktuális előfizetésbe</span><span class="sxs-lookup"><span data-stu-id="c69e3-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzureRmContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="c69e3-116">A parancs az aktuális előfizetésben a tároló csoportokat kapja.</span><span class="sxs-lookup"><span data-stu-id="c69e3-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="c69e3-117">4. példa: az erőforrás-azonosítóval kapja a tároló-csoportokat.</span><span class="sxs-lookup"><span data-stu-id="c69e3-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzureRmContainerGroup

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

<span data-ttu-id="c69e3-118">A parancs a tároló csoportot az erőforrás-azonosítóval kapja meg.</span><span class="sxs-lookup"><span data-stu-id="c69e3-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="c69e3-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c69e3-119">PARAMETERS</span></span>

### <span data-ttu-id="c69e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c69e3-120">-DefaultProfile</span></span>
<span data-ttu-id="c69e3-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c69e3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c69e3-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c69e3-122">-Name</span></span>
<span data-ttu-id="c69e3-123">A tároló csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c69e3-123">The container group Name.</span></span>

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

### <span data-ttu-id="c69e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c69e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="c69e3-125">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="c69e3-125">The resource Group Name.</span></span>

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

### <span data-ttu-id="c69e3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c69e3-126">-ResourceId</span></span>
<span data-ttu-id="c69e3-127">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="c69e3-127">The resource id.</span></span>

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

### <span data-ttu-id="c69e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c69e3-128">CommonParameters</span></span>
<span data-ttu-id="c69e3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c69e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c69e3-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c69e3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c69e3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c69e3-131">INPUTS</span></span>

### <span data-ttu-id="c69e3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c69e3-132">System.String</span></span>

## <span data-ttu-id="c69e3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c69e3-133">OUTPUTS</span></span>

### <span data-ttu-id="c69e3-134">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c69e3-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="c69e3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c69e3-135">NOTES</span></span>

## <span data-ttu-id="c69e3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c69e3-136">RELATED LINKS</span></span>
