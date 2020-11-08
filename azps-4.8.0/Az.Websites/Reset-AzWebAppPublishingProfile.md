---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025007"
---
# <span data-ttu-id="f7018-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="f7018-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="f7018-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7018-102">SYNOPSIS</span></span>

## <span data-ttu-id="f7018-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7018-103">SYNTAX</span></span>

### <span data-ttu-id="f7018-104">S1</span><span class="sxs-lookup"><span data-stu-id="f7018-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7018-105">S2</span><span class="sxs-lookup"><span data-stu-id="f7018-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7018-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7018-106">DESCRIPTION</span></span>
<span data-ttu-id="f7018-107">A **reset-AzWebAppPublishingProfile** parancsmag visszaállítja a megadott webalkalmazás közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="f7018-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="f7018-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f7018-108">EXAMPLES</span></span>

### <span data-ttu-id="f7018-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f7018-109">Example 1</span></span>

<span data-ttu-id="f7018-110">Az alábbi példa visszaállítja az erőforráscsoport MyResourceGroup társított webalkalmazás-IpRule közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="f7018-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="f7018-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7018-111">PARAMETERS</span></span>

### <span data-ttu-id="f7018-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7018-112">-DefaultProfile</span></span>
<span data-ttu-id="f7018-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7018-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7018-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7018-114">-Name</span></span>
<span data-ttu-id="f7018-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f7018-115">WebApp Name</span></span>

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

### <span data-ttu-id="f7018-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7018-116">-ResourceGroupName</span></span>
<span data-ttu-id="f7018-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f7018-117">Resource Group Name</span></span>

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

### <span data-ttu-id="f7018-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f7018-118">-WebApp</span></span>
<span data-ttu-id="f7018-119">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="f7018-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7018-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7018-120">CommonParameters</span></span>
<span data-ttu-id="f7018-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7018-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7018-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7018-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7018-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7018-123">INPUTS</span></span>

### <span data-ttu-id="f7018-124">System. String</span><span class="sxs-lookup"><span data-stu-id="f7018-124">System.String</span></span>

### <span data-ttu-id="f7018-125">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f7018-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f7018-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7018-126">OUTPUTS</span></span>

### <span data-ttu-id="f7018-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f7018-127">System.String</span></span>

## <span data-ttu-id="f7018-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7018-128">NOTES</span></span>

## <span data-ttu-id="f7018-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7018-129">RELATED LINKS</span></span>
