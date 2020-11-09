---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302839"
---
# <span data-ttu-id="ad50e-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="ad50e-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="ad50e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ad50e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad50e-103">A megadott lemezterület-titkosítási készlethez társított erőforrások listájának lekérdezése.</span><span class="sxs-lookup"><span data-stu-id="ad50e-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="ad50e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ad50e-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad50e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ad50e-105">DESCRIPTION</span></span>
<span data-ttu-id="ad50e-106">A **Get-AzDiskEncryptionSetAssociatedResource** parancsmag a megadott Lemezkezelés-készlettel társított erőforrások listáját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="ad50e-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="ad50e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ad50e-107">EXAMPLES</span></span>

### <span data-ttu-id="ad50e-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ad50e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="ad50e-109">A parancsmag kikeresi a megadott Lemezkezelés-készlettel társított két erőforrást, az "exampleDisk01" és a "exampleDisk02" kifejezést.</span><span class="sxs-lookup"><span data-stu-id="ad50e-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="ad50e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ad50e-110">PARAMETERS</span></span>

### <span data-ttu-id="ad50e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad50e-111">-DefaultProfile</span></span>
<span data-ttu-id="ad50e-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ad50e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad50e-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="ad50e-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="ad50e-114">A lemez titkosítási készletének neve.</span><span class="sxs-lookup"><span data-stu-id="ad50e-114">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="ad50e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad50e-115">-ResourceGroupName</span></span>
<span data-ttu-id="ad50e-116">Egy erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ad50e-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad50e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad50e-117">CommonParameters</span></span>
<span data-ttu-id="ad50e-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ad50e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad50e-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ad50e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad50e-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad50e-120">INPUTS</span></span>

### <span data-ttu-id="ad50e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ad50e-121">System.String</span></span>

## <span data-ttu-id="ad50e-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ad50e-122">OUTPUTS</span></span>

### <span data-ttu-id="ad50e-123">System. URI []</span><span class="sxs-lookup"><span data-stu-id="ad50e-123">System.Uri[]</span></span>

## <span data-ttu-id="ad50e-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ad50e-124">NOTES</span></span>

## <span data-ttu-id="ad50e-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ad50e-125">RELATED LINKS</span></span>
