---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 94a62f9f65be3f859b088d9e0e1d2561d097e7cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836721"
---
# <span data-ttu-id="8d1dd-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="8d1dd-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="8d1dd-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d1dd-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1dd-103">Eltávolítja a virtuális gép biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="8d1dd-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="8d1dd-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d1dd-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d1dd-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d1dd-105">DESCRIPTION</span></span>

## <span data-ttu-id="8d1dd-106">Példák</span><span class="sxs-lookup"><span data-stu-id="8d1dd-106">EXAMPLES</span></span>

### <span data-ttu-id="8d1dd-107">1:</span><span class="sxs-lookup"><span data-stu-id="8d1dd-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="8d1dd-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d1dd-108">PARAMETERS</span></span>

### <span data-ttu-id="8d1dd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1dd-109">-DefaultProfile</span></span>
<span data-ttu-id="8d1dd-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8d1dd-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d1dd-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1dd-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="8d1dd-112">-Címke</span><span class="sxs-lookup"><span data-stu-id="8d1dd-112">-Tag</span></span>
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

### <span data-ttu-id="8d1dd-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="8d1dd-113">-VMName</span></span>
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

### <span data-ttu-id="8d1dd-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1dd-114">CommonParameters</span></span>
<span data-ttu-id="8d1dd-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d1dd-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1dd-116">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d1dd-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1dd-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d1dd-117">INPUTS</span></span>

### <span data-ttu-id="8d1dd-118">System. String</span><span class="sxs-lookup"><span data-stu-id="8d1dd-118">System.String</span></span>

## <span data-ttu-id="8d1dd-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d1dd-119">OUTPUTS</span></span>

### <span data-ttu-id="8d1dd-120">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8d1dd-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8d1dd-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d1dd-121">NOTES</span></span>

## <span data-ttu-id="8d1dd-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d1dd-122">RELATED LINKS</span></span>
