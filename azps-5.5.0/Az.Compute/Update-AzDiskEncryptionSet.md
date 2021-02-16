---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDiskEncryptionSet.md
ms.openlocfilehash: 0e95179dcd2b1948b55526f3f2a8bfd5bb1a8834
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144635"
---
# <span data-ttu-id="e9a29-101">Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e9a29-101">Update-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="e9a29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a29-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a29-103">Frissíti a lemeztitkosítási készletet.</span><span class="sxs-lookup"><span data-stu-id="e9a29-103">Updates a disk encryption set.</span></span>

## <span data-ttu-id="e9a29-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e9a29-104">SYNTAX</span></span>

### <span data-ttu-id="e9a29-105">DefaultParameter (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="e9a29-105">DefaultParameter (Default)</span></span>
```
Update-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-KeyUrl <String>]
 [-SourceVaultId <String>] [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9a29-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="e9a29-106">ResourceIdParameter</span></span>
```
Update-AzDiskEncryptionSet [-ResourceId] <String> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9a29-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="e9a29-107">ObjectParameter</span></span>
```
Update-AzDiskEncryptionSet [-InputObject] <PSDiskEncryptionSet> [-KeyUrl <String>] [-SourceVaultId <String>]
 [[-Tag] <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9a29-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e9a29-108">DESCRIPTION</span></span>
<span data-ttu-id="e9a29-109">Frissíti a lemeztitkosítási készletet.</span><span class="sxs-lookup"><span data-stu-id="e9a29-109">Updates a disk encryption set.</span></span>

## <span data-ttu-id="e9a29-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e9a29-110">EXAMPLES</span></span>

### <span data-ttu-id="e9a29-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e9a29-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1;
```

<span data-ttu-id="e9a29-112">Frissíti a lemeztitkosítási készletet a kulcstár adott aktív kulcsával.</span><span class="sxs-lookup"><span data-stu-id="e9a29-112">Updates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="e9a29-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9a29-113">PARAMETERS</span></span>

### <span data-ttu-id="e9a29-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e9a29-114">-AsJob</span></span>
<span data-ttu-id="e9a29-115">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="e9a29-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9a29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a29-116">-DefaultProfile</span></span>
<span data-ttu-id="e9a29-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e9a29-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9a29-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9a29-118">-InputObject</span></span>
<span data-ttu-id="e9a29-119">A lemeztitkosítási készlet helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="e9a29-119">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="e9a29-120">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="e9a29-120">-KeyUrl</span></span>
<span data-ttu-id="e9a29-121">Az aktív kulcsra mutató URL a KeyVaultban</span><span class="sxs-lookup"><span data-stu-id="e9a29-121">Url pointing to the active key in KeyVault</span></span>

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

### <span data-ttu-id="e9a29-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e9a29-122">-Name</span></span>
<span data-ttu-id="e9a29-123">A lemeztitkosítási készlet neve.</span><span class="sxs-lookup"><span data-stu-id="e9a29-123">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="e9a29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9a29-124">-ResourceGroupName</span></span>
<span data-ttu-id="e9a29-125">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e9a29-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e9a29-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9a29-126">-ResourceId</span></span>
<span data-ttu-id="e9a29-127">Az erőforrás azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e9a29-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="e9a29-128">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e9a29-128">-SourceVaultId</span></span>
<span data-ttu-id="e9a29-129">Az aktív kulcsot tartalmazó KeyVault erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="e9a29-129">Resource id of the KeyVault containing the active key.</span></span>

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

### <span data-ttu-id="e9a29-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9a29-130">-Tag</span></span>
<span data-ttu-id="e9a29-131">Kulcsérték-párok kivonattábla formájában.</span><span class="sxs-lookup"><span data-stu-id="e9a29-131">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e9a29-132">Például: @{key0="érték0";key1=$null;key2="érték2"}</span><span class="sxs-lookup"><span data-stu-id="e9a29-132">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e9a29-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e9a29-133">-Confirm</span></span>
<span data-ttu-id="e9a29-134">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="e9a29-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a29-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a29-135">-WhatIf</span></span>
<span data-ttu-id="e9a29-136">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="e9a29-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9a29-137">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="e9a29-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9a29-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9a29-138">CommonParameters</span></span>
<span data-ttu-id="e9a29-139">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a29-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a29-140">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9a29-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a29-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e9a29-141">INPUTS</span></span>

### <span data-ttu-id="e9a29-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e9a29-142">System.String</span></span>

### <span data-ttu-id="e9a29-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e9a29-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

### <span data-ttu-id="e9a29-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e9a29-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e9a29-145">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e9a29-145">OUTPUTS</span></span>

### <span data-ttu-id="e9a29-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="e9a29-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="e9a29-147">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e9a29-147">NOTES</span></span>

## <span data-ttu-id="e9a29-148">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e9a29-148">RELATED LINKS</span></span>
