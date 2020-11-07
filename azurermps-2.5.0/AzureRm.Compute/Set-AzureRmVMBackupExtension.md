---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849686"
---
# <span data-ttu-id="6f929-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="6f929-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="6f929-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6f929-102">SYNOPSIS</span></span>
<span data-ttu-id="6f929-103">A biztonságimásolat-bővítmény tulajdonságainak megadása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="6f929-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f929-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6f929-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f929-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6f929-105">DESCRIPTION</span></span>

## <span data-ttu-id="6f929-106">Példák</span><span class="sxs-lookup"><span data-stu-id="6f929-106">EXAMPLES</span></span>

### <span data-ttu-id="6f929-107">1:</span><span class="sxs-lookup"><span data-stu-id="6f929-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="6f929-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6f929-108">PARAMETERS</span></span>

### <span data-ttu-id="6f929-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f929-109">-DefaultProfile</span></span>
<span data-ttu-id="6f929-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6f929-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f929-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6f929-111">-Name</span></span>
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

### <span data-ttu-id="6f929-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f929-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6f929-113">-Címke</span><span class="sxs-lookup"><span data-stu-id="6f929-113">-Tag</span></span>
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

### <span data-ttu-id="6f929-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="6f929-114">-VMName</span></span>
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

### <span data-ttu-id="6f929-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f929-115">CommonParameters</span></span>
<span data-ttu-id="6f929-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6f929-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f929-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f929-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f929-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f929-118">INPUTS</span></span>

### <span data-ttu-id="6f929-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="6f929-119">None</span></span>
<span data-ttu-id="6f929-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="6f929-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6f929-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6f929-121">OUTPUTS</span></span>

### <span data-ttu-id="6f929-122">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6f929-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6f929-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6f929-123">NOTES</span></span>

## <span data-ttu-id="6f929-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6f929-124">RELATED LINKS</span></span>

