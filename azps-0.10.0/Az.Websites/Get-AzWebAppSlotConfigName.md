---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EF2D377C-C000-4BCA-8EB9-58C805FA5C31
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappslotconfigname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSlotConfigName.md
ms.openlocfilehash: 414e25840b03127bbe94586248641e103c1f7d88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842762"
---
# <span data-ttu-id="65c00-101">Get-AzWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="65c00-101">Get-AzWebAppSlotConfigName</span></span>

## <span data-ttu-id="65c00-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="65c00-102">SYNOPSIS</span></span>
<span data-ttu-id="65c00-103">A Web App-bővítőhely konfigurációs neveinek listája</span><span class="sxs-lookup"><span data-stu-id="65c00-103">Get the list of Web App Slot Config names</span></span>

## <span data-ttu-id="65c00-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="65c00-104">SYNTAX</span></span>

### <span data-ttu-id="65c00-105">S1</span><span class="sxs-lookup"><span data-stu-id="65c00-105">S1</span></span>
```
Get-AzWebAppSlotConfigName [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65c00-106">S2</span><span class="sxs-lookup"><span data-stu-id="65c00-106">S2</span></span>
```
Get-AzWebAppSlotConfigName [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65c00-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="65c00-107">DESCRIPTION</span></span>
<span data-ttu-id="65c00-108">A **Get-AzWebAppSlotConfigName** parancsmag kikeresi az app beállításai és a kapcsolati karakterláncok listáját, amelyek jelenleg a bővítőhelyek beállításai szerint vannak megjelölve</span><span class="sxs-lookup"><span data-stu-id="65c00-108">The **Get-AzWebAppSlotConfigName** cmdlet retrieves the list of App Setting and Connection String names that are currently marked as slot settings</span></span>

## <span data-ttu-id="65c00-109">Példák</span><span class="sxs-lookup"><span data-stu-id="65c00-109">EXAMPLES</span></span>

### <span data-ttu-id="65c00-110">1:</span><span class="sxs-lookup"><span data-stu-id="65c00-110">1:</span></span>
```
PS C:\>Get-AzWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="65c00-111">Ez a parancs az App beállításaival és a kapcsolati karakterláncokkal függ össze az ContosoSite társított, az erőforráscsoport alapértelmezett verziójának – webes WestUS</span><span class="sxs-lookup"><span data-stu-id="65c00-111">This command gets App Settings and Connection strings pertaining to the Web App named ContosoSite associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="65c00-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="65c00-112">PARAMETERS</span></span>

### <span data-ttu-id="65c00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c00-113">-DefaultProfile</span></span>
<span data-ttu-id="65c00-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="65c00-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65c00-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="65c00-115">-Name</span></span>
<span data-ttu-id="65c00-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="65c00-116">WebApp Name</span></span>

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

### <span data-ttu-id="65c00-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65c00-117">-ResourceGroupName</span></span>
<span data-ttu-id="65c00-118">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="65c00-118">Resource Group Name</span></span>

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

### <span data-ttu-id="65c00-119">-WebApp</span><span class="sxs-lookup"><span data-stu-id="65c00-119">-WebApp</span></span>
<span data-ttu-id="65c00-120">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="65c00-120">WebApp Object</span></span>

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

### <span data-ttu-id="65c00-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c00-121">CommonParameters</span></span>
<span data-ttu-id="65c00-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="65c00-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c00-123">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c00-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c00-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="65c00-124">INPUTS</span></span>

### <span data-ttu-id="65c00-125">Webhely</span><span class="sxs-lookup"><span data-stu-id="65c00-125">Site</span></span>
<span data-ttu-id="65c00-126">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="65c00-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="65c00-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="65c00-127">OUTPUTS</span></span>

## <span data-ttu-id="65c00-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="65c00-128">NOTES</span></span>

## <span data-ttu-id="65c00-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="65c00-129">RELATED LINKS</span></span>

