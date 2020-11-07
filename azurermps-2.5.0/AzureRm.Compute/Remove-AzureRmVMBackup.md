---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850054"
---
# <span data-ttu-id="eb029-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="eb029-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="eb029-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eb029-102">SYNOPSIS</span></span>
<span data-ttu-id="eb029-103">Eltávolítja a virtuális gép biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="eb029-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb029-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eb029-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb029-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="eb029-105">DESCRIPTION</span></span>

## <span data-ttu-id="eb029-106">Példák</span><span class="sxs-lookup"><span data-stu-id="eb029-106">EXAMPLES</span></span>

### <span data-ttu-id="eb029-107">1:</span><span class="sxs-lookup"><span data-stu-id="eb029-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="eb029-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eb029-108">PARAMETERS</span></span>

### <span data-ttu-id="eb029-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb029-109">-DefaultProfile</span></span>
<span data-ttu-id="eb029-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eb029-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb029-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb029-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="eb029-112">-Címke</span><span class="sxs-lookup"><span data-stu-id="eb029-112">-Tag</span></span>
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

### <span data-ttu-id="eb029-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="eb029-113">-VMName</span></span>
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

### <span data-ttu-id="eb029-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb029-114">CommonParameters</span></span>
<span data-ttu-id="eb029-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eb029-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb029-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb029-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb029-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb029-117">INPUTS</span></span>

### <span data-ttu-id="eb029-118">Nincs</span><span class="sxs-lookup"><span data-stu-id="eb029-118">None</span></span>
<span data-ttu-id="eb029-119">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="eb029-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb029-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eb029-120">OUTPUTS</span></span>

### <span data-ttu-id="eb029-121">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="eb029-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="eb029-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eb029-122">NOTES</span></span>

## <span data-ttu-id="eb029-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eb029-123">RELATED LINKS</span></span>

