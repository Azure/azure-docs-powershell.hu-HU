---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 1f4844ae499f68031af89e801023c849577794f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836665"
---
# <span data-ttu-id="6db7f-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="6db7f-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="6db7f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6db7f-102">SYNOPSIS</span></span>
<span data-ttu-id="6db7f-103">A biztonságimásolat-bővítmény tulajdonságainak megadása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="6db7f-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="6db7f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6db7f-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6db7f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="6db7f-105">DESCRIPTION</span></span>

## <span data-ttu-id="6db7f-106">Példák</span><span class="sxs-lookup"><span data-stu-id="6db7f-106">EXAMPLES</span></span>

### <span data-ttu-id="6db7f-107">1:</span><span class="sxs-lookup"><span data-stu-id="6db7f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="6db7f-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6db7f-108">PARAMETERS</span></span>

### <span data-ttu-id="6db7f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6db7f-109">-DefaultProfile</span></span>
<span data-ttu-id="6db7f-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6db7f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6db7f-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6db7f-111">-Name</span></span>
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

### <span data-ttu-id="6db7f-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6db7f-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="6db7f-113">-Címke</span><span class="sxs-lookup"><span data-stu-id="6db7f-113">-Tag</span></span>
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

### <span data-ttu-id="6db7f-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="6db7f-114">-VMName</span></span>
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

### <span data-ttu-id="6db7f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6db7f-115">CommonParameters</span></span>
<span data-ttu-id="6db7f-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6db7f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6db7f-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6db7f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6db7f-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6db7f-118">INPUTS</span></span>

### <span data-ttu-id="6db7f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="6db7f-119">System.String</span></span>

## <span data-ttu-id="6db7f-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6db7f-120">OUTPUTS</span></span>

### <span data-ttu-id="6db7f-121">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="6db7f-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6db7f-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6db7f-122">NOTES</span></span>

## <span data-ttu-id="6db7f-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6db7f-123">RELATED LINKS</span></span>
