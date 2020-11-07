---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 02040fcb80fbf020b9d9dd3725369e75fbbf15c8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844397"
---
# <span data-ttu-id="880c3-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="880c3-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="880c3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="880c3-102">SYNOPSIS</span></span>
<span data-ttu-id="880c3-103">Eltávolítja a virtuális gép biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="880c3-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="880c3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="880c3-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="880c3-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="880c3-105">DESCRIPTION</span></span>

## <span data-ttu-id="880c3-106">Példák</span><span class="sxs-lookup"><span data-stu-id="880c3-106">EXAMPLES</span></span>

### <span data-ttu-id="880c3-107">1:</span><span class="sxs-lookup"><span data-stu-id="880c3-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="880c3-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="880c3-108">PARAMETERS</span></span>

### <span data-ttu-id="880c3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880c3-109">-DefaultProfile</span></span>
<span data-ttu-id="880c3-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="880c3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="880c3-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880c3-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="880c3-112">-Címke</span><span class="sxs-lookup"><span data-stu-id="880c3-112">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880c3-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="880c3-113">-VMName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="880c3-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880c3-114">CommonParameters</span></span>
<span data-ttu-id="880c3-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="880c3-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880c3-116">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="880c3-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880c3-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="880c3-117">INPUTS</span></span>

### <span data-ttu-id="880c3-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="880c3-118">None</span></span>
<span data-ttu-id="880c3-119">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="880c3-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="880c3-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="880c3-120">OUTPUTS</span></span>

### <span data-ttu-id="880c3-121">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="880c3-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="880c3-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="880c3-122">NOTES</span></span>

## <span data-ttu-id="880c3-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="880c3-123">RELATED LINKS</span></span>

