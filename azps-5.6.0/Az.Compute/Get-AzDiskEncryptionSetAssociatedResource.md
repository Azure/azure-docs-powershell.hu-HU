---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927265"
---
# <span data-ttu-id="cdc81-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="cdc81-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="cdc81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc81-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc81-103">A megadott lemeztitkosítási készlethez tartozó erőforrások listáját adja vissza.</span><span class="sxs-lookup"><span data-stu-id="cdc81-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="cdc81-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cdc81-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdc81-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cdc81-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc81-106">A **Get-AzDiskEncryptionSetAssociatedResource** parancsmag megkapja a megadott lemeztitkosítási készlethez társított erőforrások listáját.</span><span class="sxs-lookup"><span data-stu-id="cdc81-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="cdc81-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cdc81-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc81-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="cdc81-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="cdc81-109">A parancsmag beolvassa a megadott lemeztitkosítási készlethez társított két erőforrást (exampleDisk01 és exampleDisk02)</span><span class="sxs-lookup"><span data-stu-id="cdc81-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="cdc81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdc81-110">PARAMETERS</span></span>

### <span data-ttu-id="cdc81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc81-111">-DefaultProfile</span></span>
<span data-ttu-id="cdc81-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cdc81-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdc81-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="cdc81-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="cdc81-114">A lemeztitkosítási készlet neve.</span><span class="sxs-lookup"><span data-stu-id="cdc81-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc81-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc81-115">-ResourceGroupName</span></span>
<span data-ttu-id="cdc81-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="cdc81-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdc81-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc81-117">CommonParameters</span></span>
<span data-ttu-id="cdc81-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc81-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc81-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdc81-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc81-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdc81-120">INPUTS</span></span>

### <span data-ttu-id="cdc81-121">System.String</span><span class="sxs-lookup"><span data-stu-id="cdc81-121">System.String</span></span>

## <span data-ttu-id="cdc81-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cdc81-122">OUTPUTS</span></span>

### <span data-ttu-id="cdc81-123">System.Uri[]</span><span class="sxs-lookup"><span data-stu-id="cdc81-123">System.Uri[]</span></span>

## <span data-ttu-id="cdc81-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cdc81-124">NOTES</span></span>

## <span data-ttu-id="cdc81-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cdc81-125">RELATED LINKS</span></span>
