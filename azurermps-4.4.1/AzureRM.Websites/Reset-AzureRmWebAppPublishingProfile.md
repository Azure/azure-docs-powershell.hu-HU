---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: f1224ae7ad95598d8ae947d0e38ef3a9cf7a4dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493809"
---
# <span data-ttu-id="95cdb-101">Reset-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="95cdb-101">Reset-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="95cdb-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="95cdb-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95cdb-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="95cdb-103">SYNTAX</span></span>

### <span data-ttu-id="95cdb-104">S1</span><span class="sxs-lookup"><span data-stu-id="95cdb-104">S1</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95cdb-105">S2</span><span class="sxs-lookup"><span data-stu-id="95cdb-105">S2</span></span>
```
Reset-AzureRmWebAppPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95cdb-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="95cdb-106">DESCRIPTION</span></span>
<span data-ttu-id="95cdb-107">A **reset-AzureRmWebAppPublishingProfile** parancsmag visszaállítja a megadott webalkalmazás közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="95cdb-107">The **Reset-AzureRmWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="95cdb-108">Példák</span><span class="sxs-lookup"><span data-stu-id="95cdb-108">EXAMPLES</span></span>

### <span data-ttu-id="95cdb-109">1:</span><span class="sxs-lookup"><span data-stu-id="95cdb-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="95cdb-110">Ez a parancs visszaállítja a webalkalmazás-ContosoWebApp társított közzétételi profilt az erőforráscsoport alapértelmezett-web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="95cdb-110">This command resets the publishing profile for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="95cdb-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="95cdb-111">PARAMETERS</span></span>

### <span data-ttu-id="95cdb-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="95cdb-112">-Name</span></span>
<span data-ttu-id="95cdb-113">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="95cdb-113">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95cdb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95cdb-114">-ResourceGroupName</span></span>
<span data-ttu-id="95cdb-115">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="95cdb-115">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95cdb-116">-WebApp</span><span class="sxs-lookup"><span data-stu-id="95cdb-116">-WebApp</span></span>
<span data-ttu-id="95cdb-117">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="95cdb-117">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95cdb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95cdb-118">-DefaultProfile</span></span>
<span data-ttu-id="95cdb-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="95cdb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95cdb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95cdb-120">CommonParameters</span></span>
<span data-ttu-id="95cdb-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="95cdb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95cdb-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95cdb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95cdb-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="95cdb-123">INPUTS</span></span>

### <span data-ttu-id="95cdb-124">Webhely</span><span class="sxs-lookup"><span data-stu-id="95cdb-124">Site</span></span>
<span data-ttu-id="95cdb-125">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="95cdb-125">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="95cdb-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="95cdb-126">OUTPUTS</span></span>

## <span data-ttu-id="95cdb-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="95cdb-127">NOTES</span></span>

## <span data-ttu-id="95cdb-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="95cdb-128">RELATED LINKS</span></span>

