---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: ce07d1a46fe0f13b18238d9e20fb1d4b28b7d861
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844246"
---
# <span data-ttu-id="e63a1-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="e63a1-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="e63a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e63a1-102">SYNOPSIS</span></span>
<span data-ttu-id="e63a1-103">A biztonságimásolat-bővítmény tulajdonságainak megadása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="e63a1-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="e63a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e63a1-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e63a1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e63a1-105">DESCRIPTION</span></span>

## <span data-ttu-id="e63a1-106">Példák</span><span class="sxs-lookup"><span data-stu-id="e63a1-106">EXAMPLES</span></span>

### <span data-ttu-id="e63a1-107">1:</span><span class="sxs-lookup"><span data-stu-id="e63a1-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e63a1-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e63a1-108">PARAMETERS</span></span>

### <span data-ttu-id="e63a1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e63a1-109">-DefaultProfile</span></span>
<span data-ttu-id="e63a1-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e63a1-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e63a1-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e63a1-111">-Name</span></span>
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

### <span data-ttu-id="e63a1-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e63a1-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e63a1-113">-Címke</span><span class="sxs-lookup"><span data-stu-id="e63a1-113">-Tag</span></span>
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

### <span data-ttu-id="e63a1-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="e63a1-114">-VMName</span></span>
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

### <span data-ttu-id="e63a1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e63a1-115">CommonParameters</span></span>
<span data-ttu-id="e63a1-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e63a1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e63a1-117">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e63a1-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e63a1-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e63a1-118">INPUTS</span></span>

### <span data-ttu-id="e63a1-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="e63a1-119">None</span></span>
<span data-ttu-id="e63a1-120">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="e63a1-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e63a1-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e63a1-121">OUTPUTS</span></span>

### <span data-ttu-id="e63a1-122">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e63a1-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e63a1-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e63a1-123">NOTES</span></span>

## <span data-ttu-id="e63a1-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e63a1-124">RELATED LINKS</span></span>

