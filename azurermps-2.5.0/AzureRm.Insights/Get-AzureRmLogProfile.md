---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
ms.openlocfilehash: 29ff6159501bccd73947e25a65ec765a49b8859c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848301"
---
# <span data-ttu-id="38270-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="38270-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="38270-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="38270-102">SYNOPSIS</span></span>
<span data-ttu-id="38270-103">Log-profilt kap.</span><span class="sxs-lookup"><span data-stu-id="38270-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38270-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="38270-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38270-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="38270-105">DESCRIPTION</span></span>
<span data-ttu-id="38270-106">A **Get-AzureRmLogProfile** parancsmag naplózási profilt kap.</span><span class="sxs-lookup"><span data-stu-id="38270-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="38270-107">Példák</span><span class="sxs-lookup"><span data-stu-id="38270-107">EXAMPLES</span></span>

## <span data-ttu-id="38270-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="38270-108">PARAMETERS</span></span>

### <span data-ttu-id="38270-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38270-109">-DefaultProfile</span></span>
<span data-ttu-id="38270-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="38270-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38270-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="38270-111">-Name</span></span>
<span data-ttu-id="38270-112">A beolvasott log-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="38270-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38270-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38270-113">CommonParameters</span></span>
<span data-ttu-id="38270-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="38270-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38270-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38270-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38270-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="38270-116">INPUTS</span></span>

### <span data-ttu-id="38270-117">System. String</span><span class="sxs-lookup"><span data-stu-id="38270-117">System.String</span></span>

## <span data-ttu-id="38270-118">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38270-118">OUTPUTS</span></span>

### <span data-ttu-id="38270-119">Microsoft. Azure. commands. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="38270-119">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="38270-120">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="38270-120">NOTES</span></span>

## <span data-ttu-id="38270-121">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38270-121">RELATED LINKS</span></span>

[<span data-ttu-id="38270-122">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="38270-122">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="38270-123">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="38270-123">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


