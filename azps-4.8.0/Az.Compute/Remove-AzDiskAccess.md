---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025509"
---
# <span data-ttu-id="bf428-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="bf428-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="bf428-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf428-102">SYNOPSIS</span></span>
<span data-ttu-id="bf428-103">A Disk Access-erőforrás eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="bf428-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="bf428-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf428-104">SYNTAX</span></span>

### <span data-ttu-id="bf428-105">DefaultParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bf428-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf428-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf428-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf428-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf428-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf428-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf428-108">DESCRIPTION</span></span>
<span data-ttu-id="bf428-109">A **Remove-AzDiskAccess** parancsmag eltávolítja a Disk Access-erőforrást.</span><span class="sxs-lookup"><span data-stu-id="bf428-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="bf428-110">Példák</span><span class="sxs-lookup"><span data-stu-id="bf428-110">EXAMPLES</span></span>

### <span data-ttu-id="bf428-111">1. példa: a lemezvezérlő-hozzáférés eltávolítása alapértelmezett paraméterérték használatával</span><span class="sxs-lookup"><span data-stu-id="bf428-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="bf428-112">Ez a parancs eltávolítja a "DiskAccess01" nevű Disk Access nevű "ResourceGroup01" erőforráscsoportot</span><span class="sxs-lookup"><span data-stu-id="bf428-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="bf428-113">2. példa: a lemezvezérlő-elérés eltávolítása erőforrás-AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="bf428-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="bf428-114">A parancs erőforrás-AZONOSÍTÓval eltávolítja a lemez elérését.</span><span class="sxs-lookup"><span data-stu-id="bf428-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="bf428-115">3. példa: a beviteli objektummal való lemezellenőrzés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf428-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="bf428-116">Ez a parancs eltávolítja a InputObject által biztosított lemezterületet</span><span class="sxs-lookup"><span data-stu-id="bf428-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="bf428-117">4. példa: a csővezeték beviteli objektuma általi hozzáférés eltávolítása</span><span class="sxs-lookup"><span data-stu-id="bf428-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="bf428-118">Ez a parancs eltávolítja a InputObject</span><span class="sxs-lookup"><span data-stu-id="bf428-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="bf428-119">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf428-119">PARAMETERS</span></span>

### <span data-ttu-id="bf428-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf428-120">-AsJob</span></span>
<span data-ttu-id="bf428-121">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bf428-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf428-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf428-122">-DefaultProfile</span></span>
<span data-ttu-id="bf428-123">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bf428-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf428-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf428-124">-InputObject</span></span>
<span data-ttu-id="bf428-125">PowerShell Disk Access objektum</span><span class="sxs-lookup"><span data-stu-id="bf428-125">PowerShell Disk Access Object</span></span>

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

### <span data-ttu-id="bf428-126">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="bf428-126">-Name</span></span>
<span data-ttu-id="bf428-127">A lemez elérési útjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf428-127">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="bf428-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf428-128">-ResourceGroupName</span></span>
<span data-ttu-id="bf428-129">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf428-129">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bf428-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf428-130">-ResourceId</span></span>
<span data-ttu-id="bf428-131">A lemez eléréséhez szükséges erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="bf428-131">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="bf428-132">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="bf428-132">-Confirm</span></span>
<span data-ttu-id="bf428-133">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="bf428-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf428-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf428-134">-WhatIf</span></span>
<span data-ttu-id="bf428-135">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="bf428-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf428-136">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bf428-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf428-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf428-137">CommonParameters</span></span>
<span data-ttu-id="bf428-138">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf428-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf428-139">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="bf428-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf428-140">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf428-140">INPUTS</span></span>

### <span data-ttu-id="bf428-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bf428-141">System.String</span></span>

### <span data-ttu-id="bf428-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="bf428-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="bf428-143">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf428-143">OUTPUTS</span></span>

### <span data-ttu-id="bf428-144">Microsoft. Azure. commands. számítási. Automation. models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="bf428-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="bf428-145">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf428-145">NOTES</span></span>

## <span data-ttu-id="bf428-146">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf428-146">RELATED LINKS</span></span>
