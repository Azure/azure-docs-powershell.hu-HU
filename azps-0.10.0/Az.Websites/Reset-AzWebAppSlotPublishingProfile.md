---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/reset-Azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Reset-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: ec0b95ffee67d5597a06ed0729cded33e7489465
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842710"
---
# <span data-ttu-id="e2d00-101">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="e2d00-101">Reset-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="e2d00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e2d00-102">SYNOPSIS</span></span>

## <span data-ttu-id="e2d00-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e2d00-103">SYNTAX</span></span>

### <span data-ttu-id="e2d00-104">S1</span><span class="sxs-lookup"><span data-stu-id="e2d00-104">S1</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2d00-105">S2</span><span class="sxs-lookup"><span data-stu-id="e2d00-105">S2</span></span>
```
Reset-AzWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2d00-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="e2d00-106">DESCRIPTION</span></span>
<span data-ttu-id="e2d00-107">A **reset-AzWebAppSlotPublishingProfile** parancsmag visszaállítja a megadott webalkalmazás-bővítőhely közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="e2d00-107">The **Reset-AzWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="e2d00-108">Példák</span><span class="sxs-lookup"><span data-stu-id="e2d00-108">EXAMPLES</span></span>

### <span data-ttu-id="e2d00-109">1:</span><span class="sxs-lookup"><span data-stu-id="e2d00-109">1:</span></span>
```
PS C:\> Reset-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="e2d00-110">Ez a parancs visszaállítja a slot001 nevű bővítőhely közzétételi profilját az erőforráscsoport alapértelmezett ContosoWebApp társított, a web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e2d00-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e2d00-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e2d00-111">PARAMETERS</span></span>

### <span data-ttu-id="e2d00-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2d00-112">-DefaultProfile</span></span>
<span data-ttu-id="e2d00-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e2d00-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2d00-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e2d00-114">-Name</span></span>
<span data-ttu-id="e2d00-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="e2d00-115">WebApp Name</span></span>

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

### <span data-ttu-id="e2d00-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2d00-116">-ResourceGroupName</span></span>
<span data-ttu-id="e2d00-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="e2d00-117">Resource Group Name</span></span>

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

### <span data-ttu-id="e2d00-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="e2d00-118">-Slot</span></span>
<span data-ttu-id="e2d00-119">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="e2d00-119">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2d00-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e2d00-120">-WebApp</span></span>
<span data-ttu-id="e2d00-121">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="e2d00-121">WebApp Object</span></span>

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

### <span data-ttu-id="e2d00-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2d00-122">CommonParameters</span></span>
<span data-ttu-id="e2d00-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e2d00-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2d00-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2d00-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2d00-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2d00-125">INPUTS</span></span>

### <span data-ttu-id="e2d00-126">Webhely</span><span class="sxs-lookup"><span data-stu-id="e2d00-126">Site</span></span>
<span data-ttu-id="e2d00-127">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="e2d00-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="e2d00-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e2d00-128">OUTPUTS</span></span>

## <span data-ttu-id="e2d00-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e2d00-129">NOTES</span></span>

## <span data-ttu-id="e2d00-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e2d00-130">RELATED LINKS</span></span>

