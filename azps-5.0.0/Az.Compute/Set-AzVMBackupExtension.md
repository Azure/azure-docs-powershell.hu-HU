---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187496"
---
# <span data-ttu-id="d95fe-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="d95fe-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="d95fe-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d95fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d95fe-103">A biztonságimásolat-bővítmény tulajdonságainak megadása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="d95fe-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="d95fe-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d95fe-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d95fe-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d95fe-105">DESCRIPTION</span></span>

## <span data-ttu-id="d95fe-106">Példák</span><span class="sxs-lookup"><span data-stu-id="d95fe-106">EXAMPLES</span></span>

### <span data-ttu-id="d95fe-107">1:</span><span class="sxs-lookup"><span data-stu-id="d95fe-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="d95fe-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d95fe-108">PARAMETERS</span></span>

### <span data-ttu-id="d95fe-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95fe-109">-DefaultProfile</span></span>
<span data-ttu-id="d95fe-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d95fe-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d95fe-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d95fe-111">-Name</span></span>
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

### <span data-ttu-id="d95fe-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d95fe-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d95fe-113">-Címke</span><span class="sxs-lookup"><span data-stu-id="d95fe-113">-Tag</span></span>
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

### <span data-ttu-id="d95fe-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="d95fe-114">-VMName</span></span>
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

### <span data-ttu-id="d95fe-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95fe-115">CommonParameters</span></span>
<span data-ttu-id="d95fe-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d95fe-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95fe-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d95fe-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95fe-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d95fe-118">INPUTS</span></span>

### <span data-ttu-id="d95fe-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d95fe-119">System.String</span></span>

## <span data-ttu-id="d95fe-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d95fe-120">OUTPUTS</span></span>

### <span data-ttu-id="d95fe-121">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d95fe-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d95fe-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d95fe-122">NOTES</span></span>

## <span data-ttu-id="d95fe-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d95fe-123">RELATED LINKS</span></span>
