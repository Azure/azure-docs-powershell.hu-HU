---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: 1646bdf8265c188ccc7ba39d6154d441806967e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672160"
---
# <span data-ttu-id="16445-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="16445-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="16445-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="16445-102">SYNOPSIS</span></span>
<span data-ttu-id="16445-103">A biztonságimásolat-bővítmény tulajdonságainak megadása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="16445-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16445-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="16445-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="16445-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="16445-105">DESCRIPTION</span></span>

## <span data-ttu-id="16445-106">Példák</span><span class="sxs-lookup"><span data-stu-id="16445-106">EXAMPLES</span></span>

### <span data-ttu-id="16445-107">1:</span><span class="sxs-lookup"><span data-stu-id="16445-107">1:</span></span>
```
PS C:\> 
```

## <span data-ttu-id="16445-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="16445-108">PARAMETERS</span></span>

### <span data-ttu-id="16445-109">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="16445-109">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16445-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16445-110">-ResourceGroupName</span></span>
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

### <span data-ttu-id="16445-111">-Címke</span><span class="sxs-lookup"><span data-stu-id="16445-111">-Tag</span></span>
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

### <span data-ttu-id="16445-112">-VMName</span><span class="sxs-lookup"><span data-stu-id="16445-112">-VMName</span></span>
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

### <span data-ttu-id="16445-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16445-113">CommonParameters</span></span>
<span data-ttu-id="16445-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="16445-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16445-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16445-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16445-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="16445-116">INPUTS</span></span>

### <span data-ttu-id="16445-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="16445-117">None</span></span>
<span data-ttu-id="16445-118">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="16445-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16445-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="16445-119">OUTPUTS</span></span>

## <span data-ttu-id="16445-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="16445-120">NOTES</span></span>

## <span data-ttu-id="16445-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="16445-121">RELATED LINKS</span></span>

