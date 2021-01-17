---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480711"
---
# <span data-ttu-id="0a768-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="0a768-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="0a768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a768-102">SYNOPSIS</span></span>
<span data-ttu-id="0a768-103">Beállítja a biztonsági mentési bővítmény tulajdonságait egy virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="0a768-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="0a768-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0a768-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a768-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0a768-105">DESCRIPTION</span></span>

## <span data-ttu-id="0a768-106">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0a768-106">EXAMPLES</span></span>

### <span data-ttu-id="0a768-107">1:</span><span class="sxs-lookup"><span data-stu-id="0a768-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="0a768-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a768-108">PARAMETERS</span></span>

### <span data-ttu-id="0a768-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a768-109">-DefaultProfile</span></span>
<span data-ttu-id="0a768-110">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0a768-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a768-111">-Name</span><span class="sxs-lookup"><span data-stu-id="0a768-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a768-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a768-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="0a768-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="0a768-113">-Tag</span></span>
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

### <span data-ttu-id="0a768-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="0a768-114">-VMName</span></span>
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

### <span data-ttu-id="0a768-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a768-115">CommonParameters</span></span>
<span data-ttu-id="0a768-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a768-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a768-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0a768-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a768-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a768-118">INPUTS</span></span>

### <span data-ttu-id="0a768-119">System.String</span><span class="sxs-lookup"><span data-stu-id="0a768-119">System.String</span></span>

## <span data-ttu-id="0a768-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a768-120">OUTPUTS</span></span>

### <span data-ttu-id="0a768-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="0a768-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="0a768-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0a768-122">NOTES</span></span>

## <span data-ttu-id="0a768-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a768-123">RELATED LINKS</span></span>
