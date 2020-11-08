---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024113"
---
# <span data-ttu-id="144cc-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="144cc-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="144cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="144cc-102">SYNOPSIS</span></span>
<span data-ttu-id="144cc-103">Eltávolítja a virtuális gép biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="144cc-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="144cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="144cc-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="144cc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="144cc-105">DESCRIPTION</span></span>

## <span data-ttu-id="144cc-106">Példák</span><span class="sxs-lookup"><span data-stu-id="144cc-106">EXAMPLES</span></span>

### <span data-ttu-id="144cc-107">1:</span><span class="sxs-lookup"><span data-stu-id="144cc-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="144cc-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="144cc-108">PARAMETERS</span></span>

### <span data-ttu-id="144cc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144cc-109">-DefaultProfile</span></span>
<span data-ttu-id="144cc-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="144cc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="144cc-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="144cc-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="144cc-112">-Címke</span><span class="sxs-lookup"><span data-stu-id="144cc-112">-Tag</span></span>
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

### <span data-ttu-id="144cc-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="144cc-113">-VMName</span></span>
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

### <span data-ttu-id="144cc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144cc-114">CommonParameters</span></span>
<span data-ttu-id="144cc-115">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="144cc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144cc-116">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="144cc-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144cc-117">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="144cc-117">INPUTS</span></span>

### <span data-ttu-id="144cc-118">System. String</span><span class="sxs-lookup"><span data-stu-id="144cc-118">System.String</span></span>

## <span data-ttu-id="144cc-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="144cc-119">OUTPUTS</span></span>

### <span data-ttu-id="144cc-120">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="144cc-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="144cc-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="144cc-121">NOTES</span></span>

## <span data-ttu-id="144cc-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="144cc-122">RELATED LINKS</span></span>
