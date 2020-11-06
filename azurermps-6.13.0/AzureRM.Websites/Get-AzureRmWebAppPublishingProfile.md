---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppPublishingProfile.md
ms.openlocfilehash: a59d747dd7ba91d69d364770c91baf1a21ffedd9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494848"
---
# <span data-ttu-id="afeea-101">Get-AzureRmWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="afeea-101">Get-AzureRmWebAppPublishingProfile</span></span>

## <span data-ttu-id="afeea-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="afeea-102">SYNOPSIS</span></span>
<span data-ttu-id="afeea-103">Az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="afeea-103">Gets an Azure Web App publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afeea-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="afeea-104">SYNTAX</span></span>

### <span data-ttu-id="afeea-105">S1</span><span class="sxs-lookup"><span data-stu-id="afeea-105">S1</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="afeea-106">S2</span><span class="sxs-lookup"><span data-stu-id="afeea-106">S2</span></span>
```
Get-AzureRmWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afeea-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="afeea-107">DESCRIPTION</span></span>
<span data-ttu-id="afeea-108">A **Get-AzureRmWebAppPublishingProfile** parancsmag az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="afeea-108">The **Get-AzureRmWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="afeea-109">Példák</span><span class="sxs-lookup"><span data-stu-id="afeea-109">EXAMPLES</span></span>

### <span data-ttu-id="afeea-110">1:</span><span class="sxs-lookup"><span data-stu-id="afeea-110">1:</span></span>
```
PS C:\> Get-AzureRmWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="afeea-111">Ez a parancs beolvassa a közzétételi profilt a webalkalmazások ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának megfelelő FTP-formátumban, a webes WestUS, és a megadott kimeneti fájlban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="afeea-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="afeea-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="afeea-112">PARAMETERS</span></span>

### <span data-ttu-id="afeea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afeea-113">-DefaultProfile</span></span>
<span data-ttu-id="afeea-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="afeea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afeea-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="afeea-115">-Format</span></span>
<span data-ttu-id="afeea-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="afeea-116">Format</span></span>

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

### <span data-ttu-id="afeea-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="afeea-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="afeea-118">A katasztrófa-helyreállítási végpontok (ha igaz) befoglalása</span><span class="sxs-lookup"><span data-stu-id="afeea-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afeea-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="afeea-119">-Name</span></span>
<span data-ttu-id="afeea-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="afeea-120">WebApp Name</span></span>

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

### <span data-ttu-id="afeea-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="afeea-121">-OutputFile</span></span>
<span data-ttu-id="afeea-122">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="afeea-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afeea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afeea-123">-ResourceGroupName</span></span>
<span data-ttu-id="afeea-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="afeea-124">Resource Group Name</span></span>

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

### <span data-ttu-id="afeea-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="afeea-125">-WebApp</span></span>
<span data-ttu-id="afeea-126">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="afeea-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afeea-127">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="afeea-127">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="afeea-128">A katasztrófa-helyreállítási végpontok (ha igaz) befoglalása</span><span class="sxs-lookup"><span data-stu-id="afeea-128">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: None
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afeea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afeea-129">CommonParameters</span></span>
<span data-ttu-id="afeea-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="afeea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afeea-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afeea-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afeea-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="afeea-132">INPUTS</span></span>

### <span data-ttu-id="afeea-133">System. String</span><span class="sxs-lookup"><span data-stu-id="afeea-133">System.String</span></span>

### <span data-ttu-id="afeea-134">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="afeea-134">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="afeea-135">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="afeea-135">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="afeea-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="afeea-136">OUTPUTS</span></span>

### <span data-ttu-id="afeea-137">System. String</span><span class="sxs-lookup"><span data-stu-id="afeea-137">System.String</span></span>

## <span data-ttu-id="afeea-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="afeea-138">NOTES</span></span>

## <span data-ttu-id="afeea-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="afeea-139">RELATED LINKS</span></span>

[<span data-ttu-id="afeea-140">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="afeea-140">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)

[<span data-ttu-id="afeea-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="afeea-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


