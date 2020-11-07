---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
ms.openlocfilehash: 5884092a7520517844d6d0137023f99dc744cb86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848605"
---
# <span data-ttu-id="10b5a-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="10b5a-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="10b5a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="10b5a-103">Az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="10b5a-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10b5a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10b5a-104">SYNTAX</span></span>

### <span data-ttu-id="10b5a-105">S1</span><span class="sxs-lookup"><span data-stu-id="10b5a-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10b5a-106">S2</span><span class="sxs-lookup"><span data-stu-id="10b5a-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10b5a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="10b5a-107">DESCRIPTION</span></span>
<span data-ttu-id="10b5a-108">A **Get-AzureRmWebAppPublishingProfile** parancsmag az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="10b5a-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="10b5a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="10b5a-109">EXAMPLES</span></span>

### <span data-ttu-id="10b5a-110">1:</span><span class="sxs-lookup"><span data-stu-id="10b5a-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="10b5a-111">Ez a parancs beolvassa a közzétételi profilt a webalkalmazások ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának megfelelő FTP-formátumban, a webes WestUS, és a megadott kimeneti fájlban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="10b5a-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="10b5a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10b5a-112">PARAMETERS</span></span>

### <span data-ttu-id="10b5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b5a-113">-DefaultProfile</span></span>
<span data-ttu-id="10b5a-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10b5a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10b5a-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="10b5a-115">-Format</span></span>
<span data-ttu-id="10b5a-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="10b5a-116">Format</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b5a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10b5a-117">-Name</span></span>
<span data-ttu-id="10b5a-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="10b5a-118">WebApp Name</span></span>

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

### <span data-ttu-id="10b5a-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="10b5a-119">-OutputFile</span></span>
<span data-ttu-id="10b5a-120">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="10b5a-120">Output File</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b5a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b5a-121">-ResourceGroupName</span></span>
<span data-ttu-id="10b5a-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="10b5a-122">Resource Group Name</span></span>

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

### <span data-ttu-id="10b5a-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="10b5a-123">-WebApp</span></span>
<span data-ttu-id="10b5a-124">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="10b5a-124">WebApp Object</span></span>

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

### <span data-ttu-id="10b5a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b5a-125">CommonParameters</span></span>
<span data-ttu-id="10b5a-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10b5a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b5a-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b5a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b5a-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b5a-128">INPUTS</span></span>

### <span data-ttu-id="10b5a-129">Webhely</span><span class="sxs-lookup"><span data-stu-id="10b5a-129">Site</span></span>
<span data-ttu-id="10b5a-130">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="10b5a-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="10b5a-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10b5a-131">OUTPUTS</span></span>

## <span data-ttu-id="10b5a-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10b5a-132">NOTES</span></span>

## <span data-ttu-id="10b5a-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10b5a-133">RELATED LINKS</span></span>

[<span data-ttu-id="10b5a-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="10b5a-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="10b5a-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="10b5a-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


