---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 96e9c5945938addfbd629ef66b5f68e54c0427e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494259"
---
# <span data-ttu-id="62ae2-101">Get-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="62ae2-101">Get-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="62ae2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="62ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="62ae2-103">A Web App-bővítőhely konfigurációs neveinek listája</span><span class="sxs-lookup"><span data-stu-id="62ae2-103">Get the list of Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62ae2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="62ae2-104">SYNTAX</span></span>

### <span data-ttu-id="62ae2-105">S1</span><span class="sxs-lookup"><span data-stu-id="62ae2-105">S1</span></span>
```
Get-AzureRmWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62ae2-106">S2</span><span class="sxs-lookup"><span data-stu-id="62ae2-106">S2</span></span>
```
Get-AzureRmWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62ae2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="62ae2-107">DESCRIPTION</span></span>
<span data-ttu-id="62ae2-108">A **Get-AzureRmWebAppSlotConfigName** parancsmag kikeresi az app beállításai és a kapcsolati karakterláncok listáját, amelyek jelenleg a bővítőhelyek beállításai szerint vannak megjelölve</span><span class="sxs-lookup"><span data-stu-id="62ae2-108">The **Get-AzureRmWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="62ae2-109">Példák</span><span class="sxs-lookup"><span data-stu-id="62ae2-109">EXAMPLES</span></span>

### <span data-ttu-id="62ae2-110">1:</span><span class="sxs-lookup"><span data-stu-id="62ae2-110">1:</span></span>
```
PS C:\>Get-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="62ae2-111">Ez a parancs az App beállításaival és a kapcsolati karakterláncokkal függ össze az ContosoSite társított, az erőforráscsoport alapértelmezett verziójának – webes WestUS</span><span class="sxs-lookup"><span data-stu-id="62ae2-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="62ae2-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="62ae2-112">PARAMETERS</span></span>

### <span data-ttu-id="62ae2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ae2-113">-DefaultProfile</span></span>
<span data-ttu-id="62ae2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="62ae2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62ae2-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="62ae2-115">-Name</span></span>
<span data-ttu-id="62ae2-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="62ae2-116">WebApp Name</span></span>

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

### <span data-ttu-id="62ae2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ae2-117">-ResourceGroupName</span></span>
<span data-ttu-id="62ae2-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="62ae2-118">Resource Group Name</span></span>

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

### <span data-ttu-id="62ae2-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="62ae2-119">-WebApp</span></span>
<span data-ttu-id="62ae2-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="62ae2-120">WebApp Object</span></span>

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

### <span data-ttu-id="62ae2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ae2-121">CommonParameters</span></span>
<span data-ttu-id="62ae2-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="62ae2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ae2-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ae2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ae2-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="62ae2-124">INPUTS</span></span>

### <span data-ttu-id="62ae2-125">Webhely</span><span class="sxs-lookup"><span data-stu-id="62ae2-125">Site</span></span>
<span data-ttu-id="62ae2-126">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="62ae2-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="62ae2-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="62ae2-127">OUTPUTS</span></span>

## <span data-ttu-id="62ae2-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="62ae2-128">NOTES</span></span>

## <span data-ttu-id="62ae2-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="62ae2-129">RELATED LINKS</span></span>

