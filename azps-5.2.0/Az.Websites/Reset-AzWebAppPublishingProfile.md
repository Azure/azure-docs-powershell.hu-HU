---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326056"
---
# <span data-ttu-id="ec04a-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ec04a-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="ec04a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec04a-102">SYNOPSIS</span></span>

## <span data-ttu-id="ec04a-103">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="ec04a-103">SYNTAX</span></span>

### <span data-ttu-id="ec04a-104">S1</span><span class="sxs-lookup"><span data-stu-id="ec04a-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec04a-105">S2</span><span class="sxs-lookup"><span data-stu-id="ec04a-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec04a-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="ec04a-106">DESCRIPTION</span></span>
<span data-ttu-id="ec04a-107">A **Reset-AzWebAppPublishingProfile** parancsmag alaphelyzetbe állítja a megadott webapp közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="ec04a-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="ec04a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="ec04a-108">EXAMPLES</span></span>

### <span data-ttu-id="ec04a-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="ec04a-109">Example 1</span></span>

<span data-ttu-id="ec04a-110">Az alábbi példa alaphelyzetbe állítja a MyResourceGroup erőforráscsoporthoz társított Web App IpRule közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="ec04a-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="ec04a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec04a-111">PARAMETERS</span></span>

### <span data-ttu-id="ec04a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec04a-112">-DefaultProfile</span></span>
<span data-ttu-id="ec04a-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec04a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec04a-114">-Name</span><span class="sxs-lookup"><span data-stu-id="ec04a-114">-Name</span></span>
<span data-ttu-id="ec04a-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="ec04a-115">WebApp Name</span></span>

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

### <span data-ttu-id="ec04a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec04a-116">-ResourceGroupName</span></span>
<span data-ttu-id="ec04a-117">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="ec04a-117">Resource Group Name</span></span>

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

### <span data-ttu-id="ec04a-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ec04a-118">-WebApp</span></span>
<span data-ttu-id="ec04a-119">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="ec04a-119">WebApp Object</span></span>

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

### <span data-ttu-id="ec04a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec04a-120">CommonParameters</span></span>
<span data-ttu-id="ec04a-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec04a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec04a-122">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec04a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec04a-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec04a-123">INPUTS</span></span>

### <span data-ttu-id="ec04a-124">System.String</span><span class="sxs-lookup"><span data-stu-id="ec04a-124">System.String</span></span>

### <span data-ttu-id="ec04a-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="ec04a-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="ec04a-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec04a-126">OUTPUTS</span></span>

### <span data-ttu-id="ec04a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ec04a-127">System.String</span></span>

## <span data-ttu-id="ec04a-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="ec04a-128">NOTES</span></span>

## <span data-ttu-id="ec04a-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec04a-129">RELATED LINKS</span></span>
