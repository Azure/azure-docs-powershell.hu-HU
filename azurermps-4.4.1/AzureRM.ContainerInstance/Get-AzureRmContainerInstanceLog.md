---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 8845d9b5ac5dba0a2170e3184c866c39be29b1b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501924"
---
# <span data-ttu-id="4113a-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="4113a-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="4113a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4113a-102">SYNOPSIS</span></span>
<span data-ttu-id="4113a-103">Beolvashatja a tároló-példányok naplóit a tároló csoportban.</span><span class="sxs-lookup"><span data-stu-id="4113a-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4113a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4113a-104">SYNTAX</span></span>

### <span data-ttu-id="4113a-105">GetContainerInstanceLogByNamesParamSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4113a-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4113a-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="4113a-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4113a-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="4113a-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4113a-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4113a-108">DESCRIPTION</span></span>
<span data-ttu-id="4113a-109">A **Get-AzureRmContainerInstanceLog** parancsmag a tárolók csoportba tartozó tároló naplóit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4113a-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="4113a-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4113a-110">EXAMPLES</span></span>

### <span data-ttu-id="4113a-111">Példa 1: egy tároló-példány tail log-naplójának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4113a-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="4113a-112">A napló beszerzése `container1` tároló csoportból `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="4113a-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="4113a-113">Alapértelmezés szerint a 4MB-napló tartalmát fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="4113a-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="4113a-114">2. példa: a tároló-példányok nevével megegyező nevű tároló-példány beszerzése a farok naplójából</span><span class="sxs-lookup"><span data-stu-id="4113a-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="4113a-115">A napló beszerzése `mycontainer` tároló csoportból `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="4113a-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="4113a-116">Alapértelmezés szerint a 4MB-napló tartalmát fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="4113a-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="4113a-117">3. példa: beolvasás: a farok 2 sora a tároló példányban</span><span class="sxs-lookup"><span data-stu-id="4113a-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="4113a-118">A farok 2 sor beszerzése a `container1` tároló csoportból `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="4113a-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="4113a-119">4. példa: a tároló-példányok farok-naplójának beszerzése a vezetékes a tároló csoportban</span><span class="sxs-lookup"><span data-stu-id="4113a-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="4113a-120">A napló beolvasása a `mycontainer` vezetékes a tároló csoportban `mycontainer`</span><span class="sxs-lookup"><span data-stu-id="4113a-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="4113a-121">Alapértelmezés szerint a 4MB-napló tartalmát fogja visszaadni.</span><span class="sxs-lookup"><span data-stu-id="4113a-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="4113a-122">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4113a-122">PARAMETERS</span></span>

### <span data-ttu-id="4113a-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="4113a-123">-ContainerGroupName</span></span>
<span data-ttu-id="4113a-124">A tároló csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4113a-124">The container group name.</span></span>

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

### <span data-ttu-id="4113a-125">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4113a-125">-InputContainerGroup</span></span>
<span data-ttu-id="4113a-126">A beviteli tároló csoport objektuma.</span><span class="sxs-lookup"><span data-stu-id="4113a-126">The input container group object.</span></span>

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

### <span data-ttu-id="4113a-127">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4113a-127">-Name</span></span>
<span data-ttu-id="4113a-128">A tároló példány neve a tároló csoportban.</span><span class="sxs-lookup"><span data-stu-id="4113a-128">The container instance name in the container group.</span></span>
<span data-ttu-id="4113a-129">Alapértelmezett érték: ugyanaz, mint a tároló csoport neve</span><span class="sxs-lookup"><span data-stu-id="4113a-129">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="4113a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4113a-130">-ResourceGroupName</span></span>
<span data-ttu-id="4113a-131">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="4113a-131">The resource group name.</span></span>

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

### <span data-ttu-id="4113a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4113a-132">-ResourceId</span></span>
<span data-ttu-id="4113a-133">Az erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="4113a-133">The resource id.</span></span>

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

### <span data-ttu-id="4113a-134">-Farok</span><span class="sxs-lookup"><span data-stu-id="4113a-134">-Tail</span></span>
<span data-ttu-id="4113a-135">A naplót farok sorok száma.</span><span class="sxs-lookup"><span data-stu-id="4113a-135">The number of lines to tail the log.</span></span>
<span data-ttu-id="4113a-136">Ha nem adja meg, a parancsmag a 4MB szélű naplójába fog visszatérni</span><span class="sxs-lookup"><span data-stu-id="4113a-136">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="4113a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4113a-137">-DefaultProfile</span></span>
<span data-ttu-id="4113a-138">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4113a-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4113a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4113a-139">CommonParameters</span></span>
<span data-ttu-id="4113a-140">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4113a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4113a-141">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4113a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4113a-142">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4113a-142">INPUTS</span></span>

### <span data-ttu-id="4113a-143">Microsoft. Azure. Command. ContainerInstance. models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="4113a-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="4113a-144">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4113a-144">OUTPUTS</span></span>

### <span data-ttu-id="4113a-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4113a-145">System.String</span></span>

## <span data-ttu-id="4113a-146">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4113a-146">NOTES</span></span>

## <span data-ttu-id="4113a-147">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4113a-147">RELATED LINKS</span></span>

