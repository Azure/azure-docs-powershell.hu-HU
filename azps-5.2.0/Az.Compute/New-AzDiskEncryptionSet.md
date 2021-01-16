---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356297"
---
# <span data-ttu-id="bd444-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="bd444-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="bd444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd444-102">SYNOPSIS</span></span>
<span data-ttu-id="bd444-103">Lemeztitkosítási készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bd444-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="bd444-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="bd444-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd444-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="bd444-105">DESCRIPTION</span></span>
<span data-ttu-id="bd444-106">Lemeztitkosítási készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="bd444-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="bd444-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="bd444-107">EXAMPLES</span></span>

### <span data-ttu-id="bd444-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="bd444-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="bd444-109">Lemeztitkosítási készletet hoz létre a kulcstár adott aktív kulcsával.</span><span class="sxs-lookup"><span data-stu-id="bd444-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="bd444-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd444-110">PARAMETERS</span></span>

### <span data-ttu-id="bd444-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd444-111">-AsJob</span></span>
<span data-ttu-id="bd444-112">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="bd444-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd444-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd444-113">-DefaultProfile</span></span>
<span data-ttu-id="bd444-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bd444-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd444-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd444-115">-InputObject</span></span>
<span data-ttu-id="bd444-116">A lemeztitkosítási készlet helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="bd444-116">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="bd444-117">-Name</span><span class="sxs-lookup"><span data-stu-id="bd444-117">-Name</span></span>
<span data-ttu-id="bd444-118">A lemeztitkosítási készlet neve.</span><span class="sxs-lookup"><span data-stu-id="bd444-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="bd444-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd444-119">-ResourceGroupName</span></span>
<span data-ttu-id="bd444-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bd444-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bd444-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd444-121">-Confirm</span></span>
<span data-ttu-id="bd444-122">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="bd444-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd444-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd444-123">-WhatIf</span></span>
<span data-ttu-id="bd444-124">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="bd444-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd444-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="bd444-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd444-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd444-126">CommonParameters</span></span>
<span data-ttu-id="bd444-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd444-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd444-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd444-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd444-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd444-129">INPUTS</span></span>

### <span data-ttu-id="bd444-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bd444-130">System.String</span></span>

### <span data-ttu-id="bd444-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="bd444-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="bd444-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bd444-132">OUTPUTS</span></span>

### <span data-ttu-id="bd444-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="bd444-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="bd444-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="bd444-134">NOTES</span></span>

## <span data-ttu-id="bd444-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bd444-135">RELATED LINKS</span></span>
