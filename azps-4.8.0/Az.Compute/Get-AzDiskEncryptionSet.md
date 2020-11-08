---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94018147"
---
# <span data-ttu-id="4d4f6-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4d4f6-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="4d4f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4d4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="4d4f6-103">A lemez-titkosítási készletek beolvasása és listázása</span><span class="sxs-lookup"><span data-stu-id="4d4f6-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="4d4f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4d4f6-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d4f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="4d4f6-105">DESCRIPTION</span></span>
<span data-ttu-id="4d4f6-106">A lemez-titkosítási készletek beolvasása és listázása</span><span class="sxs-lookup"><span data-stu-id="4d4f6-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="4d4f6-107">Példák</span><span class="sxs-lookup"><span data-stu-id="4d4f6-107">EXAMPLES</span></span>

### <span data-ttu-id="4d4f6-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4d4f6-108">Example 1</span></span>
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

<span data-ttu-id="4d4f6-109">A "enc1" Lemezkezelés készletének beszerzése</span><span class="sxs-lookup"><span data-stu-id="4d4f6-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="4d4f6-110">2. példa</span><span class="sxs-lookup"><span data-stu-id="4d4f6-110">Example 2</span></span>
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

<span data-ttu-id="4d4f6-111">Az összes lemezkezelő-készlet beolvasása az erőforráscsoport "rg1" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="4d4f6-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="4d4f6-112">3. példa</span><span class="sxs-lookup"><span data-stu-id="4d4f6-112">Example 3</span></span>
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

<span data-ttu-id="4d4f6-113">Az összes lemezkezelő-készlet beszerzése az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="4d4f6-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="4d4f6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4d4f6-114">PARAMETERS</span></span>

### <span data-ttu-id="4d4f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d4f6-115">-DefaultProfile</span></span>
<span data-ttu-id="4d4f6-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4d4f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d4f6-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4d4f6-117">-Name</span></span>
<span data-ttu-id="4d4f6-118">A lemez titkosítási készletének neve.</span><span class="sxs-lookup"><span data-stu-id="4d4f6-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="4d4f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d4f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="4d4f6-120">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="4d4f6-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4d4f6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d4f6-121">CommonParameters</span></span>
<span data-ttu-id="4d4f6-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4d4f6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d4f6-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4d4f6-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d4f6-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d4f6-124">INPUTS</span></span>

### <span data-ttu-id="4d4f6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4d4f6-125">System.String</span></span>

## <span data-ttu-id="4d4f6-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4d4f6-126">OUTPUTS</span></span>

### <span data-ttu-id="4d4f6-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="4d4f6-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="4d4f6-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4d4f6-128">NOTES</span></span>

## <span data-ttu-id="4d4f6-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4d4f6-129">RELATED LINKS</span></span>
