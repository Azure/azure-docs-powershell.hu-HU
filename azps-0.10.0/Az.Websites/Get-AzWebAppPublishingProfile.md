---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 477b60400082954eb12bd0756fb4380ece2a35ad
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842766"
---
# <span data-ttu-id="917a9-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="917a9-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="917a9-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="917a9-102">SYNOPSIS</span></span>
<span data-ttu-id="917a9-103">Az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="917a9-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="917a9-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="917a9-104">SYNTAX</span></span>

### <span data-ttu-id="917a9-105">S1</span><span class="sxs-lookup"><span data-stu-id="917a9-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="917a9-106">S2</span><span class="sxs-lookup"><span data-stu-id="917a9-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="917a9-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="917a9-107">DESCRIPTION</span></span>
<span data-ttu-id="917a9-108">A **Get-AzWebAppPublishingProfile** parancsmag az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="917a9-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="917a9-109">Példák</span><span class="sxs-lookup"><span data-stu-id="917a9-109">EXAMPLES</span></span>

### <span data-ttu-id="917a9-110">1:</span><span class="sxs-lookup"><span data-stu-id="917a9-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="917a9-111">Ez a parancs beolvassa a közzétételi profilt a webalkalmazások ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának megfelelő FTP-formátumban, a webes WestUS, és a megadott kimeneti fájlban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="917a9-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="917a9-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="917a9-112">PARAMETERS</span></span>

### <span data-ttu-id="917a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917a9-113">-DefaultProfile</span></span>
<span data-ttu-id="917a9-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="917a9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="917a9-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="917a9-115">-Format</span></span>
<span data-ttu-id="917a9-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="917a9-116">Format</span></span>

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

### <span data-ttu-id="917a9-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="917a9-117">-Name</span></span>
<span data-ttu-id="917a9-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="917a9-118">WebApp Name</span></span>

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

### <span data-ttu-id="917a9-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="917a9-119">-OutputFile</span></span>
<span data-ttu-id="917a9-120">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="917a9-120">Output File</span></span>

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

### <span data-ttu-id="917a9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917a9-121">-ResourceGroupName</span></span>
<span data-ttu-id="917a9-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="917a9-122">Resource Group Name</span></span>

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

### <span data-ttu-id="917a9-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="917a9-123">-WebApp</span></span>
<span data-ttu-id="917a9-124">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="917a9-124">WebApp Object</span></span>

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

### <span data-ttu-id="917a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917a9-125">CommonParameters</span></span>
<span data-ttu-id="917a9-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="917a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917a9-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="917a9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917a9-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="917a9-128">INPUTS</span></span>

### <span data-ttu-id="917a9-129">Webhely</span><span class="sxs-lookup"><span data-stu-id="917a9-129">Site</span></span>
<span data-ttu-id="917a9-130">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="917a9-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="917a9-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="917a9-131">OUTPUTS</span></span>

## <span data-ttu-id="917a9-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="917a9-132">NOTES</span></span>

## <span data-ttu-id="917a9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="917a9-133">RELATED LINKS</span></span>

[<span data-ttu-id="917a9-134">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="917a9-134">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="917a9-135">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="917a9-135">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


