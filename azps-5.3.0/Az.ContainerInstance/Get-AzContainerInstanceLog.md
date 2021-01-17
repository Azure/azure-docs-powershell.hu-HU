---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480644"
---
# <span data-ttu-id="ee5e8-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="ee5e8-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="ee5e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5e8-103">Egy tárolócsoportban található tárolópéldány naplóinak lekérte.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="ee5e8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ee5e8-104">SYNTAX</span></span>

### <span data-ttu-id="ee5e8-105">GetContainerInstanceLogByNamesParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="ee5e8-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee5e8-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="ee5e8-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee5e8-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="ee5e8-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee5e8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ee5e8-108">DESCRIPTION</span></span>
<span data-ttu-id="ee5e8-109">A **Get-AzContainerInstanceLog** parancsmag egy tárolócsoportban található tároló naplóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="ee5e8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ee5e8-110">EXAMPLES</span></span>

### <span data-ttu-id="ee5e8-111">1. példa: Egy tárolópéldány farkanaplója</span><span class="sxs-lookup"><span data-stu-id="ee5e8-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ee5e8-112">A napló `container1` lekérte a tárolócsoportból. `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="ee5e8-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="ee5e8-113">Alapértelmezés szerint legfeljebb 4 MB-os naplótartalmat fog visszaadni.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="ee5e8-114">2. példa: A tárolócsoport nevével azonos nevű tárolópéldány naplója</span><span class="sxs-lookup"><span data-stu-id="ee5e8-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ee5e8-115">A napló `mycontainer` lekérte a tárolócsoportból. `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="ee5e8-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="ee5e8-116">Alapértelmezés szerint legfeljebb 4 MB-os naplótartalmat fog visszaadni.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="ee5e8-117">3. példa: Egy tárolópéldány 2. naplósorának lekérte</span><span class="sxs-lookup"><span data-stu-id="ee5e8-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="ee5e8-118">Szerezze be a 2 sornyi naplót a `container1` `mycontainer` tárolócsoportból.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="ee5e8-119">4. példa: Egy tárolócsoportba bevezető tárolópéldány farkanaplója</span><span class="sxs-lookup"><span data-stu-id="ee5e8-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="ee5e8-120">A naplót a `mycontainer` tárolócsoportba bepipálva szerezze `mycontainer` be.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="ee5e8-121">Alapértelmezés szerint legfeljebb 4 MB-os naplótartalmat fog visszaadni.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="ee5e8-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee5e8-122">PARAMETERS</span></span>

### <span data-ttu-id="ee5e8-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5e8-123">-ContainerGroupName</span></span>
<span data-ttu-id="ee5e8-124">A tárolócsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee5e8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5e8-125">-DefaultProfile</span></span>
<span data-ttu-id="ee5e8-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee5e8-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ee5e8-127">-InputContainerGroup</span></span>
<span data-ttu-id="ee5e8-128">A bemeneti tárolócsoport-objektum.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5e8-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ee5e8-129">-Name</span></span>
<span data-ttu-id="ee5e8-130">A tárolópéldány neve a tárolócsoportban.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-130">The container instance name in the container group.</span></span>
<span data-ttu-id="ee5e8-131">Alapértelmezett: ugyanaz, mint a tárolócsoport neve</span><span class="sxs-lookup"><span data-stu-id="ee5e8-131">Default: the same as the container group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee5e8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5e8-132">-ResourceGroupName</span></span>
<span data-ttu-id="ee5e8-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee5e8-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee5e8-134">-ResourceId</span></span>
<span data-ttu-id="ee5e8-135">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5e8-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="ee5e8-136">-Tail</span></span>
<span data-ttu-id="ee5e8-137">A naplót kiszéleső vonalak száma.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="ee5e8-138">Ha nincs meg határozva, a parancsmag legfeljebb 4 MBszélű naplót fog visszaadni</span><span class="sxs-lookup"><span data-stu-id="ee5e8-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee5e8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5e8-139">CommonParameters</span></span>
<span data-ttu-id="ee5e8-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee5e8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5e8-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee5e8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5e8-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee5e8-142">INPUTS</span></span>

### <span data-ttu-id="ee5e8-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="ee5e8-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="ee5e8-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ee5e8-144">System.String</span></span>

## <span data-ttu-id="ee5e8-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ee5e8-145">OUTPUTS</span></span>

### <span data-ttu-id="ee5e8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ee5e8-146">System.String</span></span>

## <span data-ttu-id="ee5e8-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ee5e8-147">NOTES</span></span>

## <span data-ttu-id="ee5e8-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ee5e8-148">RELATED LINKS</span></span>
