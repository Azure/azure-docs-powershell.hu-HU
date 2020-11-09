---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296444"
---
# <span data-ttu-id="3c058-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3c058-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="3c058-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c058-102">SYNOPSIS</span></span>
<span data-ttu-id="3c058-103">Megadhatja a lemez-titkosítási készlet frissítését.</span><span class="sxs-lookup"><span data-stu-id="3c058-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="3c058-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c058-104">SYNTAX</span></span>

### <span data-ttu-id="3c058-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3c058-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c058-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="3c058-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3c058-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="3c058-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3c058-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c058-108">DESCRIPTION</span></span>
<span data-ttu-id="3c058-109">Megadhatja a lemez-titkosítási készlet frissítését.</span><span class="sxs-lookup"><span data-stu-id="3c058-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="3c058-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3c058-110">EXAMPLES</span></span>

### <span data-ttu-id="3c058-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="3c058-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="3c058-112">A kulcsfájl frissíti a merevlemez-titkosítási készletet az adott aktív kulccsal.</span><span class="sxs-lookup"><span data-stu-id="3c058-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="3c058-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c058-113">PARAMETERS</span></span>

### <span data-ttu-id="3c058-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c058-114">-AsJob</span></span>
<span data-ttu-id="3c058-115">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="3c058-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c058-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c058-116">-DefaultProfile</span></span>
<span data-ttu-id="3c058-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c058-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c058-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c058-118">-InputObject</span></span>
<span data-ttu-id="3c058-119">A merevlemez-titkosítási készlet helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="3c058-119">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: ObjectParameter
Aliases: DiskEncryptionSet

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c058-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="3c058-120">-KeyUrl</span></span>
<span data-ttu-id="3c058-121">Az aktív kulcsra mutató URL-cím a betárcsázón</span><span class="sxs-lookup"><span data-stu-id="3c058-121">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c058-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3c058-122">-Name</span></span>
<span data-ttu-id="3c058-123">A lemez titkosítási készletének neve.</span><span class="sxs-lookup"><span data-stu-id="3c058-123">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c058-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c058-124">-ResourceGroupName</span></span>
<span data-ttu-id="3c058-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="3c058-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c058-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c058-126">-ResourceId</span></span>
<span data-ttu-id="3c058-127">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c058-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c058-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3c058-128">-SourceVaultId</span></span>
<span data-ttu-id="3c058-129">Az aktív kulcsot tartalmazó kulcskezelő erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="3c058-129">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c058-130">-Címke</span><span class="sxs-lookup"><span data-stu-id="3c058-130">-Tag</span></span>
<span data-ttu-id="3c058-131">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="3c058-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3c058-132">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="3c058-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c058-133">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="3c058-133">-Confirm</span></span>
<span data-ttu-id="3c058-134">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="3c058-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c058-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c058-135">-WhatIf</span></span>
<span data-ttu-id="3c058-136">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="3c058-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c058-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="3c058-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c058-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c058-138">CommonParameters</span></span>
<span data-ttu-id="3c058-139">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c058-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c058-140">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="3c058-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c058-141">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c058-141">INPUTS</span></span>

### <span data-ttu-id="3c058-142">System. String</span><span class="sxs-lookup"><span data-stu-id="3c058-142">System.String</span></span>

### <span data-ttu-id="3c058-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3c058-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="3c058-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3c058-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3c058-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c058-145">OUTPUTS</span></span>

### <span data-ttu-id="3c058-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="3c058-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="3c058-147">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c058-147">NOTES</span></span>

## <span data-ttu-id="3c058-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c058-148">RELATED LINKS</span></span>
