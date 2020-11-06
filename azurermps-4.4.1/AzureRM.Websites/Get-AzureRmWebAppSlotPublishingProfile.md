---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: d8ccd8f1011a73068c24323bb86e39340dfc9573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495506"
---
# <span data-ttu-id="ec69b-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ec69b-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="ec69b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ec69b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec69b-103">Beilleszt egy Azure Web App bővítőhely-közzétételi profilt.</span><span class="sxs-lookup"><span data-stu-id="ec69b-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec69b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ec69b-104">SYNTAX</span></span>

### <span data-ttu-id="ec69b-105">S1</span><span class="sxs-lookup"><span data-stu-id="ec69b-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec69b-106">S2</span><span class="sxs-lookup"><span data-stu-id="ec69b-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec69b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ec69b-107">DESCRIPTION</span></span>
<span data-ttu-id="ec69b-108">A **Get-AzureRmWebAppSlotPublishingProfile** parancsmag a webalkalmazás közzétételi profilját kapja meg a megadott bővítőhelyhez.</span><span class="sxs-lookup"><span data-stu-id="ec69b-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="ec69b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ec69b-109">EXAMPLES</span></span>

### <span data-ttu-id="ec69b-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="ec69b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="ec69b-111">Ez a parancs beolvassa a közzétételi profilt FTP-formátumban, amely az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp van társítva – a web-WestUS, és a megadott kimeneti fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="ec69b-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="ec69b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ec69b-112">PARAMETERS</span></span>

### <span data-ttu-id="ec69b-113">Formátumú</span><span class="sxs-lookup"><span data-stu-id="ec69b-113">-Format</span></span>
<span data-ttu-id="ec69b-114">Formázása</span><span class="sxs-lookup"><span data-stu-id="ec69b-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec69b-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ec69b-115">-Name</span></span>
<span data-ttu-id="ec69b-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="ec69b-116">WebApp Name</span></span>

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

### <span data-ttu-id="ec69b-117">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="ec69b-117">-OutputFile</span></span>
<span data-ttu-id="ec69b-118">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="ec69b-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec69b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec69b-119">-ResourceGroupName</span></span>
<span data-ttu-id="ec69b-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ec69b-120">Resource Group Name</span></span>

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

### <span data-ttu-id="ec69b-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="ec69b-121">-Slot</span></span>
<span data-ttu-id="ec69b-122">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="ec69b-122">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec69b-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ec69b-123">-WebApp</span></span>
<span data-ttu-id="ec69b-124">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="ec69b-124">WebApp Object</span></span>

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

### <span data-ttu-id="ec69b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec69b-125">-DefaultProfile</span></span>
<span data-ttu-id="ec69b-126">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ec69b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec69b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec69b-127">CommonParameters</span></span>
<span data-ttu-id="ec69b-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ec69b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec69b-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec69b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec69b-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec69b-130">INPUTS</span></span>

### <span data-ttu-id="ec69b-131">Webhely</span><span class="sxs-lookup"><span data-stu-id="ec69b-131">Site</span></span>
<span data-ttu-id="ec69b-132">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ec69b-132">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ec69b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ec69b-133">OUTPUTS</span></span>

## <span data-ttu-id="ec69b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ec69b-134">NOTES</span></span>

## <span data-ttu-id="ec69b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ec69b-135">RELATED LINKS</span></span>

[<span data-ttu-id="ec69b-136">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ec69b-136">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="ec69b-137">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ec69b-137">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ec69b-138">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ec69b-138">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
