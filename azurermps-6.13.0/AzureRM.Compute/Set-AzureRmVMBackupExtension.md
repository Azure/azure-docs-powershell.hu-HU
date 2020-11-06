---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: 5a8f82168db41305042e976b9daa1828b2072f95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494102"
---
# <span data-ttu-id="3f0dc-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="3f0dc-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="3f0dc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3f0dc-102">SYNOPSIS</span></span>
<span data-ttu-id="3f0dc-103">A biztonságimásolat-bővítmény tulajdonságainak megadása virtuális gépen.</span><span class="sxs-lookup"><span data-stu-id="3f0dc-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f0dc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3f0dc-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f0dc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="3f0dc-105">DESCRIPTION</span></span>

## <span data-ttu-id="3f0dc-106">Példák</span><span class="sxs-lookup"><span data-stu-id="3f0dc-106">EXAMPLES</span></span>

### <span data-ttu-id="3f0dc-107">1:</span><span class="sxs-lookup"><span data-stu-id="3f0dc-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="3f0dc-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3f0dc-108">PARAMETERS</span></span>

### <span data-ttu-id="3f0dc-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f0dc-109">-DefaultProfile</span></span>
<span data-ttu-id="3f0dc-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f0dc-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f0dc-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="3f0dc-111">-Name</span></span>
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

### <span data-ttu-id="3f0dc-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f0dc-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3f0dc-113">-Címke</span><span class="sxs-lookup"><span data-stu-id="3f0dc-113">-Tag</span></span>
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

### <span data-ttu-id="3f0dc-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="3f0dc-114">-VMName</span></span>
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

### <span data-ttu-id="3f0dc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f0dc-115">CommonParameters</span></span>
<span data-ttu-id="3f0dc-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3f0dc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f0dc-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f0dc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f0dc-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f0dc-118">INPUTS</span></span>

### <span data-ttu-id="3f0dc-119">System. String</span><span class="sxs-lookup"><span data-stu-id="3f0dc-119">System.String</span></span>

## <span data-ttu-id="3f0dc-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f0dc-120">OUTPUTS</span></span>

### <span data-ttu-id="3f0dc-121">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3f0dc-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3f0dc-122">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3f0dc-122">NOTES</span></span>

## <span data-ttu-id="3f0dc-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f0dc-123">RELATED LINKS</span></span>
