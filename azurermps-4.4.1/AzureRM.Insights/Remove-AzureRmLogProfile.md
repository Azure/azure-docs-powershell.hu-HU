---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: DDA137FD-4EB3-4FB7-A202-978922038AFC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmLogProfile.md
ms.openlocfilehash: f931f0ffb38af251be3ffb213b61f7033bb59150
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679079"
---
# <span data-ttu-id="e92fa-101">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="e92fa-101">Remove-AzureRmLogProfile</span></span>

## <span data-ttu-id="e92fa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e92fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e92fa-103">A napló-profil eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="e92fa-103">Removes a log profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e92fa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e92fa-104">SYNTAX</span></span>

```
Remove-AzureRmLogProfile -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e92fa-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e92fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e92fa-106">A **Remove-AzureRmLogProfile** parancsmag eltávolít egy log-profilt.</span><span class="sxs-lookup"><span data-stu-id="e92fa-106">The **Remove-AzureRmLogProfile** cmdlet removes a log profile.</span></span>

## <span data-ttu-id="e92fa-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e92fa-107">EXAMPLES</span></span>

## <span data-ttu-id="e92fa-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e92fa-108">PARAMETERS</span></span>

### <span data-ttu-id="e92fa-109">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e92fa-109">-Name</span></span>
<span data-ttu-id="e92fa-110">Az eltávolítandó naplózási profil nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e92fa-110">Specifies the name of the log profile to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e92fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e92fa-111">-DefaultProfile</span></span>
<span data-ttu-id="e92fa-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e92fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e92fa-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e92fa-113">-PassThru</span></span>
<span data-ttu-id="e92fa-114">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e92fa-114">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e92fa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e92fa-115">CommonParameters</span></span>
<span data-ttu-id="e92fa-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e92fa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e92fa-117">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e92fa-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e92fa-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e92fa-118">INPUTS</span></span>

## <span data-ttu-id="e92fa-119">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e92fa-119">OUTPUTS</span></span>

### <span data-ttu-id="e92fa-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e92fa-120">System.Boolean</span></span>

## <span data-ttu-id="e92fa-121">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e92fa-121">NOTES</span></span>

## <span data-ttu-id="e92fa-122">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e92fa-122">RELATED LINKS</span></span>

[<span data-ttu-id="e92fa-123">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="e92fa-123">Add-AzureRmLogProfile</span></span>](./Add-AzureRmLogProfile.md)

[<span data-ttu-id="e92fa-124">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="e92fa-124">Get-AzureRmLogProfile</span></span>](./Get-AzureRmLogProfile.md)


