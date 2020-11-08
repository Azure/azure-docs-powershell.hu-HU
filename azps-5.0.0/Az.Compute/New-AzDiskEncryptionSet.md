---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186247"
---
# <span data-ttu-id="cfff8-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cfff8-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="cfff8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfff8-102">SYNOPSIS</span></span>
<span data-ttu-id="cfff8-103">Lemez-titkosítási készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cfff8-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="cfff8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfff8-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfff8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfff8-105">DESCRIPTION</span></span>
<span data-ttu-id="cfff8-106">Lemez-titkosítási készletet hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cfff8-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="cfff8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cfff8-107">EXAMPLES</span></span>

### <span data-ttu-id="cfff8-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cfff8-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="cfff8-109">A kulcs-tárolóban az adott aktív kulcs segítségével hozza létre a Lemezkezelés bővítményt.</span><span class="sxs-lookup"><span data-stu-id="cfff8-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="cfff8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfff8-110">PARAMETERS</span></span>

### <span data-ttu-id="cfff8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfff8-111">-AsJob</span></span>
<span data-ttu-id="cfff8-112">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="cfff8-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfff8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfff8-113">-DefaultProfile</span></span>
<span data-ttu-id="cfff8-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfff8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfff8-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfff8-115">-InputObject</span></span>
<span data-ttu-id="cfff8-116">A merevlemez-titkosítási készlet helyi objektuma.</span><span class="sxs-lookup"><span data-stu-id="cfff8-116">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="cfff8-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cfff8-117">-Name</span></span>
<span data-ttu-id="cfff8-118">A lemez titkosítási készletének neve.</span><span class="sxs-lookup"><span data-stu-id="cfff8-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="cfff8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfff8-119">-ResourceGroupName</span></span>
<span data-ttu-id="cfff8-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cfff8-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cfff8-121">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="cfff8-121">-Confirm</span></span>
<span data-ttu-id="cfff8-122">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="cfff8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfff8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfff8-123">-WhatIf</span></span>
<span data-ttu-id="cfff8-124">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="cfff8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfff8-125">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="cfff8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfff8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfff8-126">CommonParameters</span></span>
<span data-ttu-id="cfff8-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfff8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfff8-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="cfff8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfff8-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfff8-129">INPUTS</span></span>

### <span data-ttu-id="cfff8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cfff8-130">System.String</span></span>

### <span data-ttu-id="cfff8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cfff8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="cfff8-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfff8-132">OUTPUTS</span></span>

### <span data-ttu-id="cfff8-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cfff8-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="cfff8-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfff8-134">NOTES</span></span>

## <span data-ttu-id="cfff8-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfff8-135">RELATED LINKS</span></span>
