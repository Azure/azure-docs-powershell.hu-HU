---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100144802"
---
# <span data-ttu-id="fb4cc-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="fb4cc-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="fb4cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4cc-103">Eltávolítja a biztonsági másolatot egy virtuális gépről.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="fb4cc-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="fb4cc-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb4cc-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="fb4cc-105">DESCRIPTION</span></span>

## <span data-ttu-id="fb4cc-106">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="fb4cc-106">EXAMPLES</span></span>

### <span data-ttu-id="fb4cc-107">1:</span><span class="sxs-lookup"><span data-stu-id="fb4cc-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="fb4cc-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb4cc-108">PARAMETERS</span></span>

### <span data-ttu-id="fb4cc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4cc-109">-DefaultProfile</span></span>
<span data-ttu-id="fb4cc-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb4cc-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb4cc-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fb4cc-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb4cc-112">-Tag</span></span>
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

### <span data-ttu-id="fb4cc-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="fb4cc-113">-VMName</span></span>
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

### <span data-ttu-id="fb4cc-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4cc-114">CommonParameters</span></span>
<span data-ttu-id="fb4cc-115">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb4cc-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4cc-116">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb4cc-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4cc-117">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fb4cc-117">INPUTS</span></span>

### <span data-ttu-id="fb4cc-118">System.String</span><span class="sxs-lookup"><span data-stu-id="fb4cc-118">System.String</span></span>

## <span data-ttu-id="fb4cc-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fb4cc-119">OUTPUTS</span></span>

### <span data-ttu-id="fb4cc-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fb4cc-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fb4cc-121">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="fb4cc-121">NOTES</span></span>

## <span data-ttu-id="fb4cc-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fb4cc-122">RELATED LINKS</span></span>
