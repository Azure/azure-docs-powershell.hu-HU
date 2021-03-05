---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: 2ab0102534a8773ca1ca206bde2075e2bd7930f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012261"
---
# <span data-ttu-id="84843-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="84843-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="84843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84843-102">SYNOPSIS</span></span>
<span data-ttu-id="84843-103">Egy tárolócsoportban található tárolópéldány naplóinak lekérte.</span><span class="sxs-lookup"><span data-stu-id="84843-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="84843-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="84843-104">SYNTAX</span></span>

### <span data-ttu-id="84843-105">GetContainerInstanceLogByNamesParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="84843-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84843-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="84843-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84843-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="84843-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84843-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="84843-108">DESCRIPTION</span></span>
<span data-ttu-id="84843-109">A **Get-AzContainerInstanceLog** parancsmag egy tárolócsoportban található tároló naplóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="84843-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="84843-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="84843-110">EXAMPLES</span></span>

### <span data-ttu-id="84843-111">1. példa: Egy tárolópéldány farkanaplója</span><span class="sxs-lookup"><span data-stu-id="84843-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="84843-112">A napló `container1` lekérte a tárolócsoportból. `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="84843-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="84843-113">Alapértelmezés szerint legfeljebb 4 MB-os naplótartalmat fog visszaadni.</span><span class="sxs-lookup"><span data-stu-id="84843-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="84843-114">2. példa: A tárolócsoport nevével azonos nevű tárolópéldány naplója</span><span class="sxs-lookup"><span data-stu-id="84843-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="84843-115">A napló `mycontainer` lekérte a tárolócsoportból. `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="84843-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="84843-116">Alapértelmezés szerint legfeljebb 4 MB-os naplótartalmat fog visszaadni.</span><span class="sxs-lookup"><span data-stu-id="84843-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="84843-117">3. példa: Egy tárolópéldány 2. naplósorának lekérte</span><span class="sxs-lookup"><span data-stu-id="84843-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="84843-118">Szerezze be a 2 sornyi naplót a `container1` `mycontainer` tárolócsoportból.</span><span class="sxs-lookup"><span data-stu-id="84843-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="84843-119">4. példa: Egy tárolócsoportba bevezető tárolópéldány farkanaplója</span><span class="sxs-lookup"><span data-stu-id="84843-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="84843-120">A naplót a `mycontainer` tárolócsoportba bevezető naplóból szerezze `mycontainer` be.</span><span class="sxs-lookup"><span data-stu-id="84843-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="84843-121">Alapértelmezés szerint legfeljebb 4 MB-os naplótartalmat fog visszaadni.</span><span class="sxs-lookup"><span data-stu-id="84843-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="84843-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84843-122">PARAMETERS</span></span>

### <span data-ttu-id="84843-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="84843-123">-ContainerGroupName</span></span>
<span data-ttu-id="84843-124">A tárolócsoport neve.</span><span class="sxs-lookup"><span data-stu-id="84843-124">The container group name.</span></span>

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

### <span data-ttu-id="84843-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84843-125">-DefaultProfile</span></span>
<span data-ttu-id="84843-126">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="84843-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84843-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="84843-127">-InputContainerGroup</span></span>
<span data-ttu-id="84843-128">A bemeneti tárolócsoport-objektum.</span><span class="sxs-lookup"><span data-stu-id="84843-128">The input container group object.</span></span>

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

### <span data-ttu-id="84843-129">-Name</span><span class="sxs-lookup"><span data-stu-id="84843-129">-Name</span></span>
<span data-ttu-id="84843-130">A tárolópéldány neve a tárolócsoportban.</span><span class="sxs-lookup"><span data-stu-id="84843-130">The container instance name in the container group.</span></span>
<span data-ttu-id="84843-131">Alapértelmezett: ugyanaz, mint a tárolócsoport neve</span><span class="sxs-lookup"><span data-stu-id="84843-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="84843-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84843-132">-ResourceGroupName</span></span>
<span data-ttu-id="84843-133">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="84843-133">The resource group name.</span></span>

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

### <span data-ttu-id="84843-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84843-134">-ResourceId</span></span>
<span data-ttu-id="84843-135">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="84843-135">The resource id.</span></span>

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

### <span data-ttu-id="84843-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="84843-136">-Tail</span></span>
<span data-ttu-id="84843-137">A naplót kiszéleső vonalak száma.</span><span class="sxs-lookup"><span data-stu-id="84843-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="84843-138">Ha nincs meg határozva, a parancsmag legfeljebb 4 MBszélű naplót fog visszaadni</span><span class="sxs-lookup"><span data-stu-id="84843-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="84843-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84843-139">CommonParameters</span></span>
<span data-ttu-id="84843-140">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84843-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84843-141">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84843-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84843-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84843-142">INPUTS</span></span>

### <span data-ttu-id="84843-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="84843-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="84843-144">System.String</span><span class="sxs-lookup"><span data-stu-id="84843-144">System.String</span></span>

## <span data-ttu-id="84843-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="84843-145">OUTPUTS</span></span>

### <span data-ttu-id="84843-146">System.String</span><span class="sxs-lookup"><span data-stu-id="84843-146">System.String</span></span>

## <span data-ttu-id="84843-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="84843-147">NOTES</span></span>

## <span data-ttu-id="84843-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="84843-148">RELATED LINKS</span></span>
