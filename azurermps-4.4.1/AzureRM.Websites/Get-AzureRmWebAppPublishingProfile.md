---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a05dfcbf509ccb68c0b928467a5695361a4916e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494588"
---
# <span data-ttu-id="ca726-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="ca726-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="ca726-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ca726-102">SYNOPSIS</span></span>
<span data-ttu-id="ca726-103">Az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="ca726-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca726-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ca726-104">SYNTAX</span></span>

### <span data-ttu-id="ca726-105">S1</span><span class="sxs-lookup"><span data-stu-id="ca726-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca726-106">S2</span><span class="sxs-lookup"><span data-stu-id="ca726-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [-OutputFile] <String> [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca726-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="ca726-107">DESCRIPTION</span></span>
<span data-ttu-id="ca726-108">A **Get-AzureRmWebAppPublishingProfile** parancsmag az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="ca726-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="ca726-109">Példák</span><span class="sxs-lookup"><span data-stu-id="ca726-109">EXAMPLES</span></span>

### <span data-ttu-id="ca726-110">1:</span><span class="sxs-lookup"><span data-stu-id="ca726-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="ca726-111">Ez a parancs beolvassa a közzétételi profilt a webalkalmazások ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának megfelelő FTP-formátumban, a webes WestUS, és a megadott kimeneti fájlban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="ca726-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="ca726-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ca726-112">PARAMETERS</span></span>

### <span data-ttu-id="ca726-113">Formátumú</span><span class="sxs-lookup"><span data-stu-id="ca726-113">-Format</span></span>
<span data-ttu-id="ca726-114">Formázása</span><span class="sxs-lookup"><span data-stu-id="ca726-114">Format</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: WebDeploy, FileZilla3, Ftp

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca726-115">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="ca726-115">-Name</span></span>
<span data-ttu-id="ca726-116">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="ca726-116">WebApp Name</span></span>

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

### <span data-ttu-id="ca726-117">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="ca726-117">-OutputFile</span></span>
<span data-ttu-id="ca726-118">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="ca726-118">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca726-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca726-119">-ResourceGroupName</span></span>
<span data-ttu-id="ca726-120">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="ca726-120">Resource Group Name</span></span>

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

### <span data-ttu-id="ca726-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ca726-121">-WebApp</span></span>
<span data-ttu-id="ca726-122">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="ca726-122">WebApp Object</span></span>

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

### <span data-ttu-id="ca726-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca726-123">-DefaultProfile</span></span>
<span data-ttu-id="ca726-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ca726-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca726-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca726-125">CommonParameters</span></span>
<span data-ttu-id="ca726-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ca726-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca726-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca726-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca726-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca726-128">INPUTS</span></span>

### <span data-ttu-id="ca726-129">Webhely</span><span class="sxs-lookup"><span data-stu-id="ca726-129">Site</span></span>
<span data-ttu-id="ca726-130">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="ca726-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ca726-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ca726-131">OUTPUTS</span></span>

## <span data-ttu-id="ca726-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ca726-132">NOTES</span></span>

## <span data-ttu-id="ca726-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ca726-133">RELATED LINKS</span></span>

[<span data-ttu-id="ca726-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="ca726-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="ca726-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ca726-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


