---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94185722"
---
# <span data-ttu-id="902be-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="902be-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="902be-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="902be-102">SYNOPSIS</span></span>
<span data-ttu-id="902be-103">A Disk Access-erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="902be-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="902be-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="902be-104">SYNTAX</span></span>

### <span data-ttu-id="902be-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="902be-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="902be-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="902be-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="902be-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="902be-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="902be-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="902be-108">DESCRIPTION</span></span>
<span data-ttu-id="902be-109">A **Remove-AzDiskAccess** parancsmag eltávolítja a Disk Access-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="902be-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="902be-110">Példák</span><span class="sxs-lookup"><span data-stu-id="902be-110">EXAMPLES</span></span>

### <span data-ttu-id="902be-111">1. példa: a lemezvezérlő-hozzáférés eltávolítása alapértelmezett paraméterérték használatával</span><span class="sxs-lookup"><span data-stu-id="902be-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="902be-112">Ez a parancs eltávolítja a "DiskAccess01" nevű Disk Access nevű "ResourceGroup01" erőforráscsoportot</span><span class="sxs-lookup"><span data-stu-id="902be-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="902be-113">2. példa: a lemezvezérlő-elérés eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="902be-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="902be-114">A parancs erőforrás-AZONOSÍTÓval eltávolítja a lemez elérését.</span><span class="sxs-lookup"><span data-stu-id="902be-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="902be-115">3. példa: a beviteli objektummal való lemezellenőrzés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="902be-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="902be-116">Ez a parancs eltávolítja a InputObject által biztosított lemezterületet</span><span class="sxs-lookup"><span data-stu-id="902be-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="902be-117">4. példa: a csővezeték beviteli objektuma általi hozzáférés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="902be-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="902be-118">Ez a parancs eltávolítja a InputObject</span><span class="sxs-lookup"><span data-stu-id="902be-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="902be-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="902be-119">PARAMETERS</span></span>

### <span data-ttu-id="902be-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="902be-120">-AsJob</span></span>
<span data-ttu-id="902be-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="902be-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="902be-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="902be-122">-DefaultProfile</span></span>
<span data-ttu-id="902be-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="902be-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="902be-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="902be-124">-InputObject</span></span>
<span data-ttu-id="902be-125">PowerShell Disk Access objektum</span><span class="sxs-lookup"><span data-stu-id="902be-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="902be-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="902be-126">-Name</span></span>
<span data-ttu-id="902be-127">A lemez elérési útjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="902be-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902be-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="902be-128">-ResourceGroupName</span></span>
<span data-ttu-id="902be-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="902be-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902be-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="902be-130">-ResourceId</span></span>
<span data-ttu-id="902be-131">A lemez eléréséhez szükséges erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="902be-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902be-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="902be-132">-Confirm</span></span>
<span data-ttu-id="902be-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="902be-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="902be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="902be-134">-WhatIf</span></span>
<span data-ttu-id="902be-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="902be-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="902be-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="902be-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="902be-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902be-137">CommonParameters</span></span>
<span data-ttu-id="902be-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="902be-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902be-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="902be-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902be-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="902be-140">INPUTS</span></span>

### <span data-ttu-id="902be-141">System. String</span><span class="sxs-lookup"><span data-stu-id="902be-141">System.String</span></span>

### <span data-ttu-id="902be-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="902be-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="902be-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="902be-143">OUTPUTS</span></span>

### <span data-ttu-id="902be-144">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="902be-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="902be-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="902be-145">NOTES</span></span>

## <span data-ttu-id="902be-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="902be-146">RELATED LINKS</span></span>
