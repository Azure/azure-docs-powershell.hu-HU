---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3CD449A1-084E-4950-80EF-06B5ECDFB70F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/reset-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Reset-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 352b0bc196745aba3c5eeda357e0727a9ea3e4c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498652"
---
# <span data-ttu-id="08108-101">Reset-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="08108-101">Reset-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="08108-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="08108-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08108-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="08108-103">SYNTAX</span></span>

### <span data-ttu-id="08108-104">S1</span><span class="sxs-lookup"><span data-stu-id="08108-104">S1</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08108-105">S2</span><span class="sxs-lookup"><span data-stu-id="08108-105">S2</span></span>
```
Reset-AzureRmWebAppSlotPublishingProfile [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="08108-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="08108-106">DESCRIPTION</span></span>
<span data-ttu-id="08108-107">A **reset-AzureRmWebAppSlotPublishingProfile** parancsmag visszaállítja a megadott webalkalmazás-bővítőhely közzétételi profilját.</span><span class="sxs-lookup"><span data-stu-id="08108-107">The **Reset-AzureRmWebAppSlotPublishingProfile** cmdlet resets the publishing profile for the specified Web App Slot.</span></span>

## <span data-ttu-id="08108-108">Példák</span><span class="sxs-lookup"><span data-stu-id="08108-108">EXAMPLES</span></span>

### <span data-ttu-id="08108-109">1:</span><span class="sxs-lookup"><span data-stu-id="08108-109">1:</span></span>
```
PS C:\> Reset-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001"
```

<span data-ttu-id="08108-110">Ez a parancs visszaállítja a slot001 nevű bővítőhely közzétételi profilját az erőforráscsoport alapértelmezett ContosoWebApp társított, a web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="08108-110">This command resets the publishing profile for the Slot named slot001 for the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="08108-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="08108-111">PARAMETERS</span></span>

### <span data-ttu-id="08108-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08108-112">-DefaultProfile</span></span>
<span data-ttu-id="08108-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08108-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08108-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="08108-114">-Name</span></span>
<span data-ttu-id="08108-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="08108-115">WebApp Name</span></span>

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

### <span data-ttu-id="08108-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08108-116">-ResourceGroupName</span></span>
<span data-ttu-id="08108-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="08108-117">Resource Group Name</span></span>

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

### <span data-ttu-id="08108-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="08108-118">-Slot</span></span>
<span data-ttu-id="08108-119">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="08108-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="08108-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="08108-120">-WebApp</span></span>
<span data-ttu-id="08108-121">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="08108-121">WebApp Object</span></span>

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

### <span data-ttu-id="08108-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08108-122">CommonParameters</span></span>
<span data-ttu-id="08108-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="08108-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08108-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08108-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08108-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="08108-125">INPUTS</span></span>

### <span data-ttu-id="08108-126">Webhely</span><span class="sxs-lookup"><span data-stu-id="08108-126">Site</span></span>
<span data-ttu-id="08108-127">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="08108-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="08108-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08108-128">OUTPUTS</span></span>

## <span data-ttu-id="08108-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="08108-129">NOTES</span></span>

## <span data-ttu-id="08108-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08108-130">RELATED LINKS</span></span>

