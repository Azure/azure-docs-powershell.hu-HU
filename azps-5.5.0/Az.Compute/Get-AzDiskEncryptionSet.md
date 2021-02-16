---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148955"
---
# <span data-ttu-id="49218-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="49218-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="49218-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49218-102">SYNOPSIS</span></span>
<span data-ttu-id="49218-103">Lemeztitkosítási készletek lekért vagy listába sorolt.</span><span class="sxs-lookup"><span data-stu-id="49218-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="49218-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="49218-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49218-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="49218-105">DESCRIPTION</span></span>
<span data-ttu-id="49218-106">Lemeztitkosítási készletek lekért vagy listába sorolt.</span><span class="sxs-lookup"><span data-stu-id="49218-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="49218-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="49218-107">EXAMPLES</span></span>

### <span data-ttu-id="49218-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="49218-108">Example 1</span></span>
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

<span data-ttu-id="49218-109">Az "enc1" lemeztitkosítási készlet lekérte</span><span class="sxs-lookup"><span data-stu-id="49218-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="49218-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="49218-110">Example 2</span></span>
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

<span data-ttu-id="49218-111">Szerezze be az összes lemeztitkosítási készletet az "rg1" erőforráscsoportban.</span><span class="sxs-lookup"><span data-stu-id="49218-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="49218-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="49218-112">Example 3</span></span>
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

<span data-ttu-id="49218-113">Szerezze be az előfizetés összes lemeztitkosítási készletét.</span><span class="sxs-lookup"><span data-stu-id="49218-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="49218-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49218-114">PARAMETERS</span></span>

### <span data-ttu-id="49218-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49218-115">-DefaultProfile</span></span>
<span data-ttu-id="49218-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="49218-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49218-117">-Name</span><span class="sxs-lookup"><span data-stu-id="49218-117">-Name</span></span>
<span data-ttu-id="49218-118">A lemeztitkosítási készlet neve.</span><span class="sxs-lookup"><span data-stu-id="49218-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="49218-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49218-119">-ResourceGroupName</span></span>
<span data-ttu-id="49218-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="49218-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="49218-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49218-121">CommonParameters</span></span>
<span data-ttu-id="49218-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49218-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49218-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49218-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49218-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="49218-124">INPUTS</span></span>

### <span data-ttu-id="49218-125">System.String</span><span class="sxs-lookup"><span data-stu-id="49218-125">System.String</span></span>

## <span data-ttu-id="49218-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="49218-126">OUTPUTS</span></span>

### <span data-ttu-id="49218-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="49218-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="49218-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="49218-128">NOTES</span></span>

## <span data-ttu-id="49218-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="49218-129">RELATED LINKS</span></span>
