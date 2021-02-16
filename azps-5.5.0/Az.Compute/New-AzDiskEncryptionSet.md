---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148867"
---
# <span data-ttu-id="d2c89-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d2c89-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="d2c89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2c89-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c89-103">Lemeztitkosítási készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d2c89-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="d2c89-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d2c89-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2c89-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d2c89-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c89-106">Lemeztitkosítási készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d2c89-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="d2c89-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d2c89-107">EXAMPLES</span></span>

### <span data-ttu-id="d2c89-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="d2c89-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="d2c89-109">Lemeztitkosítási készletet hoz létre a kulcstár adott aktív kulcsával.</span><span class="sxs-lookup"><span data-stu-id="d2c89-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="d2c89-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2c89-110">PARAMETERS</span></span>

### <span data-ttu-id="d2c89-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2c89-111">-AsJob</span></span>
<span data-ttu-id="d2c89-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="d2c89-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2c89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c89-113">-DefaultProfile</span></span>
<span data-ttu-id="d2c89-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d2c89-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2c89-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2c89-115">-InputObject</span></span>
<span data-ttu-id="d2c89-116">A lemeztitkosítási készlet helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="d2c89-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c89-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d2c89-117">-Name</span></span>
<span data-ttu-id="d2c89-118">A lemeztitkosítási készlet neve.</span><span class="sxs-lookup"><span data-stu-id="d2c89-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c89-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2c89-119">-ResourceGroupName</span></span>
<span data-ttu-id="d2c89-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d2c89-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c89-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2c89-121">-Confirm</span></span>
<span data-ttu-id="d2c89-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="d2c89-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2c89-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2c89-123">-WhatIf</span></span>
<span data-ttu-id="d2c89-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="d2c89-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2c89-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="d2c89-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2c89-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c89-126">CommonParameters</span></span>
<span data-ttu-id="d2c89-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c89-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c89-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2c89-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c89-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2c89-129">INPUTS</span></span>

### <span data-ttu-id="d2c89-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d2c89-130">System.String</span></span>

### <span data-ttu-id="d2c89-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d2c89-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="d2c89-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d2c89-132">OUTPUTS</span></span>

### <span data-ttu-id="d2c89-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="d2c89-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="d2c89-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d2c89-134">NOTES</span></span>

## <span data-ttu-id="d2c89-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d2c89-135">RELATED LINKS</span></span>
