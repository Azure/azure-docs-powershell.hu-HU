---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
ms.openlocfilehash: 17ad6612ff36539d212c20c2321c6292fb63a499
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849874"
---
# <span data-ttu-id="92bca-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="92bca-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="92bca-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="92bca-102">SYNOPSIS</span></span>
<span data-ttu-id="92bca-103">Beilleszt egy Azure Web App bővítőhely-közzétételi profilt.</span><span class="sxs-lookup"><span data-stu-id="92bca-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92bca-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="92bca-104">SYNTAX</span></span>

### <span data-ttu-id="92bca-105">S1</span><span class="sxs-lookup"><span data-stu-id="92bca-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92bca-106">S2</span><span class="sxs-lookup"><span data-stu-id="92bca-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92bca-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="92bca-107">DESCRIPTION</span></span>
<span data-ttu-id="92bca-108">A **Get-AzureRmWebAppSlotPublishingProfile** parancsmag a webalkalmazás közzétételi profilját kapja meg a megadott bővítőhelyhez.</span><span class="sxs-lookup"><span data-stu-id="92bca-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="92bca-109">Példák</span><span class="sxs-lookup"><span data-stu-id="92bca-109">EXAMPLES</span></span>

### <span data-ttu-id="92bca-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="92bca-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="92bca-111">Ez a parancs beolvassa a közzétételi profilt FTP-formátumban, amely az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp van társítva – a web-WestUS, és a megadott kimeneti fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="92bca-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="92bca-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="92bca-112">PARAMETERS</span></span>

### <span data-ttu-id="92bca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92bca-113">-DefaultProfile</span></span>
<span data-ttu-id="92bca-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="92bca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92bca-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="92bca-115">-Format</span></span>
<span data-ttu-id="92bca-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="92bca-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bca-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="92bca-117">-Name</span></span>
<span data-ttu-id="92bca-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="92bca-118">WebApp Name</span></span>

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

### <span data-ttu-id="92bca-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="92bca-119">-OutputFile</span></span>
<span data-ttu-id="92bca-120">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="92bca-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92bca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92bca-121">-ResourceGroupName</span></span>
<span data-ttu-id="92bca-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="92bca-122">Resource Group Name</span></span>

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

### <span data-ttu-id="92bca-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="92bca-123">-Slot</span></span>
<span data-ttu-id="92bca-124">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="92bca-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="92bca-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="92bca-125">-WebApp</span></span>
<span data-ttu-id="92bca-126">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="92bca-126">WebApp Object</span></span>

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

### <span data-ttu-id="92bca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92bca-127">CommonParameters</span></span>
<span data-ttu-id="92bca-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="92bca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92bca-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92bca-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92bca-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="92bca-130">INPUTS</span></span>

### <span data-ttu-id="92bca-131">Webhely</span><span class="sxs-lookup"><span data-stu-id="92bca-131">Site</span></span>
<span data-ttu-id="92bca-132">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="92bca-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="92bca-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="92bca-133">OUTPUTS</span></span>

## <span data-ttu-id="92bca-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="92bca-134">NOTES</span></span>

## <span data-ttu-id="92bca-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="92bca-135">RELATED LINKS</span></span>

[<span data-ttu-id="92bca-136">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="92bca-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="92bca-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="92bca-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="92bca-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="92bca-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
