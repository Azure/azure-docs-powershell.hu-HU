---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: f082241be9e31b11782fcbbf5570a7f3c3947012
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848050"
---
# <span data-ttu-id="64fc5-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="64fc5-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="64fc5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="64fc5-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64fc5-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="64fc5-103">SYNTAX</span></span>

### <span data-ttu-id="64fc5-104">S1</span><span class="sxs-lookup"><span data-stu-id="64fc5-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64fc5-105">S2</span><span class="sxs-lookup"><span data-stu-id="64fc5-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64fc5-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="64fc5-106">DESCRIPTION</span></span>
<span data-ttu-id="64fc5-107">A **reset-AzureRmWebAppPublishingProfile** parancsmag visszaállítja a megadott webalkalmazás közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="64fc5-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="64fc5-108">Példák</span><span class="sxs-lookup"><span data-stu-id="64fc5-108">EXAMPLES</span></span>

### <span data-ttu-id="64fc5-109">1:</span><span class="sxs-lookup"><span data-stu-id="64fc5-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="64fc5-110">Ez a parancs visszaállítja a webalkalmazás-ContosoWebApp társított közzétételi profilt az erőforráscsoport alapértelmezett-web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="64fc5-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="64fc5-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="64fc5-111">PARAMETERS</span></span>

### <span data-ttu-id="64fc5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64fc5-112">-DefaultProfile</span></span>
<span data-ttu-id="64fc5-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="64fc5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64fc5-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="64fc5-114">-Name</span></span>
<span data-ttu-id="64fc5-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="64fc5-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64fc5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64fc5-116">-ResourceGroupName</span></span>
<span data-ttu-id="64fc5-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="64fc5-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64fc5-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="64fc5-118">-WebApp</span></span>
<span data-ttu-id="64fc5-119">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="64fc5-119">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64fc5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64fc5-120">CommonParameters</span></span>
<span data-ttu-id="64fc5-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="64fc5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64fc5-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64fc5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64fc5-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="64fc5-123">INPUTS</span></span>

### <span data-ttu-id="64fc5-124">Webhely</span><span class="sxs-lookup"><span data-stu-id="64fc5-124">Site</span></span>
<span data-ttu-id="64fc5-125">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="64fc5-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="64fc5-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="64fc5-126">OUTPUTS</span></span>

## <span data-ttu-id="64fc5-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="64fc5-127">NOTES</span></span>

## <span data-ttu-id="64fc5-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="64fc5-128">RELATED LINKS</span></span>

