---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: 1202d15504717052513f1ef77a21e008fefe20af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492958"
---
# <span data-ttu-id="0006c-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="0006c-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="0006c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0006c-102">SYNOPSIS</span></span>
<span data-ttu-id="0006c-103">Az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="0006c-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0006c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0006c-104">SYNTAX</span></span>

### <span data-ttu-id="0006c-105">S1</span><span class="sxs-lookup"><span data-stu-id="0006c-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0006c-106">S2</span><span class="sxs-lookup"><span data-stu-id="0006c-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0006c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0006c-107">DESCRIPTION</span></span>
<span data-ttu-id="0006c-108">A **Get-AzureRmWebAppPublishingProfile** parancsmag az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="0006c-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="0006c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0006c-109">EXAMPLES</span></span>

### <span data-ttu-id="0006c-110">1:</span><span class="sxs-lookup"><span data-stu-id="0006c-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="0006c-111">Ez a parancs beolvassa a közzétételi profilt a webalkalmazások ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának megfelelő FTP-formátumban, a webes WestUS, és a megadott kimeneti fájlban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="0006c-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="0006c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0006c-112">PARAMETERS</span></span>

### <span data-ttu-id="0006c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0006c-113">-DefaultProfile</span></span>
<span data-ttu-id="0006c-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0006c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0006c-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="0006c-115">-Format</span></span>
<span data-ttu-id="0006c-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="0006c-116">Format</span></span>

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

### <span data-ttu-id="0006c-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0006c-117">-Name</span></span>
<span data-ttu-id="0006c-118">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="0006c-118">WebApp Name</span></span>

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

### <span data-ttu-id="0006c-119">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="0006c-119">-OutputFile</span></span>
<span data-ttu-id="0006c-120">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="0006c-120">Output File</span></span>

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

### <span data-ttu-id="0006c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0006c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0006c-122">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0006c-122">Resource Group Name</span></span>

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

### <span data-ttu-id="0006c-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0006c-123">-WebApp</span></span>
<span data-ttu-id="0006c-124">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="0006c-124">WebApp Object</span></span>

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

### <span data-ttu-id="0006c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0006c-125">CommonParameters</span></span>
<span data-ttu-id="0006c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0006c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0006c-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0006c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0006c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0006c-128">INPUTS</span></span>

### <span data-ttu-id="0006c-129">Webhely</span><span class="sxs-lookup"><span data-stu-id="0006c-129">Site</span></span>
<span data-ttu-id="0006c-130">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="0006c-130">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="0006c-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0006c-131">OUTPUTS</span></span>

## <span data-ttu-id="0006c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0006c-132">NOTES</span></span>

## <span data-ttu-id="0006c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0006c-133">RELATED LINKS</span></span>

[<span data-ttu-id="0006c-134">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0006c-134">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="0006c-135">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="0006c-135">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


