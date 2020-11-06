---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 019EFD94-4087-45F6-812D-FBDFE1B2E48A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermlogprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmLogProfile.md
ms.openlocfilehash: b96c8717e20395c57e6c9d5d4520327d97dfa174
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495347"
---
# <span data-ttu-id="ca30d-101">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="ca30d-101">Get-AzureRmLogProfile</span></span>

## <span data-ttu-id="ca30d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca30d-102">SYNOPSIS</span></span>
<span data-ttu-id="ca30d-103">Log-profilt kap.</span><span class="sxs-lookup"><span data-stu-id="ca30d-103">Gets a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca30d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca30d-104">SYNTAX</span></span>

```
Get-AzureRmLogProfile [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca30d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca30d-105">DESCRIPTION</span></span>
<span data-ttu-id="ca30d-106">A **Get-AzureRmLogProfile** parancsmag naplózási profilt kap.</span><span class="sxs-lookup"><span data-stu-id="ca30d-106">The **Get-AzureRmLogProfile** cmdlet gets a log profile.</span></span>

## <span data-ttu-id="ca30d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ca30d-107">EXAMPLES</span></span>

## <span data-ttu-id="ca30d-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca30d-108">PARAMETERS</span></span>

### <span data-ttu-id="ca30d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca30d-109">-DefaultProfile</span></span>
<span data-ttu-id="ca30d-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="ca30d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca30d-111">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca30d-111">-Name</span></span>
<span data-ttu-id="ca30d-112">A beolvasott log-profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="ca30d-112">Specifies the name of the log profile to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca30d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca30d-113">CommonParameters</span></span>
<span data-ttu-id="ca30d-114">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca30d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca30d-115">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca30d-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca30d-116">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca30d-116">INPUTS</span></span>

### <span data-ttu-id="ca30d-117">Nincs</span><span class="sxs-lookup"><span data-stu-id="ca30d-117">None</span></span>
<span data-ttu-id="ca30d-118">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="ca30d-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ca30d-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca30d-119">OUTPUTS</span></span>

### <span data-ttu-id="ca30d-120">Microsoft. Azure. commands. OutputClasses. PSLogProfileCollection</span><span class="sxs-lookup"><span data-stu-id="ca30d-120">Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfileCollection</span></span>

## <span data-ttu-id="ca30d-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca30d-121">NOTES</span></span>

## <span data-ttu-id="ca30d-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca30d-122">RELATED LINKS</span></span>

[<span data-ttu-id="ca30d-123">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="ca30d-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="ca30d-124">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="ca30d-124">Remove-AzureRmLogProfile</span></span>](./Remove-AzureRmLogProfile.md)


