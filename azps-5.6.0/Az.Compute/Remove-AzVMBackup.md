---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 23ae31c79c33e9299d1cf3dc5998798657408da4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928658"
---
# <span data-ttu-id="76448-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="76448-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="76448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76448-102">SYNOPSIS</span></span>
<span data-ttu-id="76448-103">Eltávolítja a biztonsági másolatot egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="76448-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="76448-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="76448-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76448-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="76448-105">DESCRIPTION</span></span>

## <span data-ttu-id="76448-106">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="76448-106">EXAMPLES</span></span>

### <span data-ttu-id="76448-107">1:</span><span class="sxs-lookup"><span data-stu-id="76448-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="76448-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76448-108">PARAMETERS</span></span>

### <span data-ttu-id="76448-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76448-109">-DefaultProfile</span></span>
<span data-ttu-id="76448-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="76448-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76448-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76448-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="76448-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="76448-112">-Tag</span></span>
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

### <span data-ttu-id="76448-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="76448-113">-VMName</span></span>
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

### <span data-ttu-id="76448-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76448-114">CommonParameters</span></span>
<span data-ttu-id="76448-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76448-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76448-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76448-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76448-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76448-117">INPUTS</span></span>

### <span data-ttu-id="76448-118">System.String</span><span class="sxs-lookup"><span data-stu-id="76448-118">System.String</span></span>

## <span data-ttu-id="76448-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="76448-119">OUTPUTS</span></span>

### <span data-ttu-id="76448-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="76448-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="76448-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="76448-121">NOTES</span></span>

## <span data-ttu-id="76448-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="76448-122">RELATED LINKS</span></span>
