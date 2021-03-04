---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 344bba00d610b5e23b2af5bce8476185e8bee377
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927273"
---
# <span data-ttu-id="c8c37-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c8c37-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="c8c37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8c37-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c37-103">Lemeztitkosítási készletek lekért vagy listába sorolt.</span><span class="sxs-lookup"><span data-stu-id="c8c37-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="c8c37-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c8c37-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8c37-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c8c37-105">DESCRIPTION</span></span>
<span data-ttu-id="c8c37-106">Lemeztitkosítási készletek lekért vagy listába sorolt.</span><span class="sxs-lookup"><span data-stu-id="c8c37-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="c8c37-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c8c37-107">EXAMPLES</span></span>

### <span data-ttu-id="c8c37-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="c8c37-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="c8c37-109">Az "enc1" lemeztitkosítási készlet lekérte</span><span class="sxs-lookup"><span data-stu-id="c8c37-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="c8c37-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="c8c37-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="c8c37-111">Szerezze be az "rg1" erőforráscsoport összes lemeztitkosítási készletét.</span><span class="sxs-lookup"><span data-stu-id="c8c37-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="c8c37-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="c8c37-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="c8c37-113">Szerezze be az előfizetés összes lemeztitkosítási készletét.</span><span class="sxs-lookup"><span data-stu-id="c8c37-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="c8c37-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8c37-114">PARAMETERS</span></span>

### <span data-ttu-id="c8c37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c37-115">-DefaultProfile</span></span>
<span data-ttu-id="c8c37-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c8c37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c37-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c8c37-117">-Name</span></span>
<span data-ttu-id="c8c37-118">A lemeztitkosítási készlet neve.</span><span class="sxs-lookup"><span data-stu-id="c8c37-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c37-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c37-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8c37-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="c8c37-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8c37-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c37-121">CommonParameters</span></span>
<span data-ttu-id="c8c37-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c37-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c37-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8c37-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c37-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8c37-124">INPUTS</span></span>

### <span data-ttu-id="c8c37-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c8c37-125">System.String</span></span>

## <span data-ttu-id="c8c37-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c8c37-126">OUTPUTS</span></span>

### <span data-ttu-id="c8c37-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="c8c37-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="c8c37-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c8c37-128">NOTES</span></span>

## <span data-ttu-id="c8c37-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c8c37-129">RELATED LINKS</span></span>
