---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 519a072a0c51f489a78992e483dec8aa9cd1fab5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842713"
---
# <span data-ttu-id="a2222-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="a2222-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="a2222-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a2222-102">SYNOPSIS</span></span>

## <span data-ttu-id="a2222-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a2222-103">SYNTAX</span></span>

### <span data-ttu-id="a2222-104">S1</span><span class="sxs-lookup"><span data-stu-id="a2222-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2222-105">S2</span><span class="sxs-lookup"><span data-stu-id="a2222-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2222-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="a2222-106">DESCRIPTION</span></span>
<span data-ttu-id="a2222-107">A **reset-AzWebAppPublishingProfile** parancsmag visszaállítja a megadott webalkalmazás közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="a2222-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="a2222-108">Példák</span><span class="sxs-lookup"><span data-stu-id="a2222-108">EXAMPLES</span></span>

### <span data-ttu-id="a2222-109">1:</span><span class="sxs-lookup"><span data-stu-id="a2222-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a2222-110">Ez a parancs visszaállítja a webalkalmazás-ContosoWebApp társított közzétételi profilt az erőforráscsoport alapértelmezett-web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a2222-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="a2222-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a2222-111">PARAMETERS</span></span>

### <span data-ttu-id="a2222-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2222-112">-DefaultProfile</span></span>
<span data-ttu-id="a2222-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a2222-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2222-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a2222-114">-Name</span></span>
<span data-ttu-id="a2222-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="a2222-115">WebApp Name</span></span>

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

### <span data-ttu-id="a2222-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2222-116">-ResourceGroupName</span></span>
<span data-ttu-id="a2222-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="a2222-117">Resource Group Name</span></span>

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

### <span data-ttu-id="a2222-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a2222-118">-WebApp</span></span>
<span data-ttu-id="a2222-119">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="a2222-119">WebApp Object</span></span>

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

### <span data-ttu-id="a2222-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2222-120">CommonParameters</span></span>
<span data-ttu-id="a2222-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a2222-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2222-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2222-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2222-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2222-123">INPUTS</span></span>

### <span data-ttu-id="a2222-124">Webhely</span><span class="sxs-lookup"><span data-stu-id="a2222-124">Site</span></span>
<span data-ttu-id="a2222-125">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="a2222-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a2222-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a2222-126">OUTPUTS</span></span>

## <span data-ttu-id="a2222-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a2222-127">NOTES</span></span>

## <span data-ttu-id="a2222-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a2222-128">RELATED LINKS</span></span>

