---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
ms.openlocfilehash: cb28249d5c32119d187becd8b07f2137f3f312d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672117"
---
# <span data-ttu-id="790fa-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="790fa-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="790fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="790fa-102">SYNOPSIS</span></span>
<span data-ttu-id="790fa-103">Eltávolítja a virtuális gép biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="790fa-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="790fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="790fa-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="790fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="790fa-105">DESCRIPTION</span></span>

## <span data-ttu-id="790fa-106">Példák</span><span class="sxs-lookup"><span data-stu-id="790fa-106">EXAMPLES</span></span>

### <span data-ttu-id="790fa-107">1:</span><span class="sxs-lookup"><span data-stu-id="790fa-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="790fa-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="790fa-108">PARAMETERS</span></span>

### <span data-ttu-id="790fa-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="790fa-109">-DefaultProfile</span></span>
<span data-ttu-id="790fa-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="790fa-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="790fa-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="790fa-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="790fa-112">-Címke</span><span class="sxs-lookup"><span data-stu-id="790fa-112">-Tag</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="790fa-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="790fa-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="790fa-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="790fa-114">CommonParameters</span></span>
<span data-ttu-id="790fa-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="790fa-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="790fa-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="790fa-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="790fa-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="790fa-117">INPUTS</span></span>

### <span data-ttu-id="790fa-118">System. String</span><span class="sxs-lookup"><span data-stu-id="790fa-118">System.String</span></span>

## <span data-ttu-id="790fa-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="790fa-119">OUTPUTS</span></span>

### <span data-ttu-id="790fa-120">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="790fa-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="790fa-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="790fa-121">NOTES</span></span>

## <span data-ttu-id="790fa-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="790fa-122">RELATED LINKS</span></span>
