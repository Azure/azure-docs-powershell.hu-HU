---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011170"
---
# <span data-ttu-id="af7b7-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="af7b7-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="af7b7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="af7b7-102">SYNOPSIS</span></span>
<span data-ttu-id="af7b7-103">Beolvashatja a tároló-példányok naplóit a tároló csoportban.</span><span class="sxs-lookup"><span data-stu-id="af7b7-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="af7b7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="af7b7-104">SYNTAX</span></span>

### <span data-ttu-id="af7b7-105">GetContainerInstanceLogByNamesParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="af7b7-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af7b7-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="af7b7-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af7b7-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="af7b7-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af7b7-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="af7b7-108">DESCRIPTION</span></span>
<span data-ttu-id="af7b7-109">A **Get-AzContainerInstanceLog** parancsmag a tárolók csoportba tartozó tároló naplóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="af7b7-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="af7b7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="af7b7-110">EXAMPLES</span></span>

### <span data-ttu-id="af7b7-111">Példa 1: egy tároló-példány tail log-naplójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="af7b7-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="af7b7-112">A napló beszerzése `container1` tároló csoportból `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="af7b7-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="af7b7-113">Alapértelmezés szerint a 4MB-napló tartalmát fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="af7b7-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="af7b7-114">2. példa: a tároló-példányok nevével megegyező nevű tároló-példány beszerzése a farok naplójából</span><span class="sxs-lookup"><span data-stu-id="af7b7-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="af7b7-115">A napló beszerzése `mycontainer` tároló csoportból `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="af7b7-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="af7b7-116">Alapértelmezés szerint a 4MB-napló tartalmát fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="af7b7-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="af7b7-117">3. példa: beolvasás: a farok 2 sora a tároló példányban</span><span class="sxs-lookup"><span data-stu-id="af7b7-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="af7b7-118">A farok 2 sor beszerzése a `container1` tároló csoportból `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="af7b7-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="af7b7-119">4. példa: a tároló-példányok farok-naplójának beszerzése a vezetékes a tároló csoportban</span><span class="sxs-lookup"><span data-stu-id="af7b7-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="af7b7-120">A napló beolvasása a `mycontainer` vezetékes a tároló csoportban `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="af7b7-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="af7b7-121">Alapértelmezés szerint a 4MB-napló tartalmát fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="af7b7-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="af7b7-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="af7b7-122">PARAMETERS</span></span>

### <span data-ttu-id="af7b7-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="af7b7-123">-ContainerGroupName</span></span>
<span data-ttu-id="af7b7-124">A tároló csoport neve.</span><span class="sxs-lookup"><span data-stu-id="af7b7-124">The container group name.</span></span>

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

### <span data-ttu-id="af7b7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7b7-125">-DefaultProfile</span></span>
<span data-ttu-id="af7b7-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="af7b7-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af7b7-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="af7b7-127">-InputContainerGroup</span></span>
<span data-ttu-id="af7b7-128">A beviteli tároló csoport objektuma.</span><span class="sxs-lookup"><span data-stu-id="af7b7-128">The input container group object.</span></span>

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

### <span data-ttu-id="af7b7-129">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="af7b7-129">-Name</span></span>
<span data-ttu-id="af7b7-130">A tároló példány neve a tároló csoportban.</span><span class="sxs-lookup"><span data-stu-id="af7b7-130">The container instance name in the container group.</span></span>
<span data-ttu-id="af7b7-131">Alapértelmezett érték: ugyanaz, mint a tároló csoport neve</span><span class="sxs-lookup"><span data-stu-id="af7b7-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="af7b7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af7b7-132">-ResourceGroupName</span></span>
<span data-ttu-id="af7b7-133">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="af7b7-133">The resource group name.</span></span>

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

### <span data-ttu-id="af7b7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af7b7-134">-ResourceId</span></span>
<span data-ttu-id="af7b7-135">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="af7b7-135">The resource id.</span></span>

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

### <span data-ttu-id="af7b7-136">-Farok</span><span class="sxs-lookup"><span data-stu-id="af7b7-136">-Tail</span></span>
<span data-ttu-id="af7b7-137">A naplót farok sorok száma.</span><span class="sxs-lookup"><span data-stu-id="af7b7-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="af7b7-138">Ha nem adja meg, a parancsmag a 4MB szélű naplójába fog visszatérni</span><span class="sxs-lookup"><span data-stu-id="af7b7-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="af7b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7b7-139">CommonParameters</span></span>
<span data-ttu-id="af7b7-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="af7b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7b7-141">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7b7-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7b7-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="af7b7-142">INPUTS</span></span>

### <span data-ttu-id="af7b7-143">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="af7b7-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="af7b7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="af7b7-144">System.String</span></span>

## <span data-ttu-id="af7b7-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="af7b7-145">OUTPUTS</span></span>

### <span data-ttu-id="af7b7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="af7b7-146">System.String</span></span>

## <span data-ttu-id="af7b7-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="af7b7-147">NOTES</span></span>

## <span data-ttu-id="af7b7-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="af7b7-148">RELATED LINKS</span></span>
