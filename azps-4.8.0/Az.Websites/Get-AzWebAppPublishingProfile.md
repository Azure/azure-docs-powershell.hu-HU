---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 4e4e8e1575070f04a02496014ab93276a2dc9328
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183126"
---
# <span data-ttu-id="24d6f-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="24d6f-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="24d6f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="24d6f-102">SYNOPSIS</span></span>
<span data-ttu-id="24d6f-103">Az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="24d6f-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="24d6f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="24d6f-104">SYNTAX</span></span>

### <span data-ttu-id="24d6f-105">S1</span><span class="sxs-lookup"><span data-stu-id="24d6f-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24d6f-106">S2</span><span class="sxs-lookup"><span data-stu-id="24d6f-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24d6f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="24d6f-107">DESCRIPTION</span></span>
<span data-ttu-id="24d6f-108">A **Get-AzWebAppPublishingProfile** parancsmag az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="24d6f-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="24d6f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="24d6f-109">EXAMPLES</span></span>

### <span data-ttu-id="24d6f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="24d6f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="24d6f-111">Ez a parancs beolvassa a közzétételi profilt a webalkalmazások ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának megfelelő FTP-formátumban, a webes WestUS, és a megadott kimeneti fájlban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="24d6f-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="24d6f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="24d6f-112">PARAMETERS</span></span>

### <span data-ttu-id="24d6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d6f-113">-DefaultProfile</span></span>
<span data-ttu-id="24d6f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="24d6f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d6f-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="24d6f-115">-Format</span></span>
<span data-ttu-id="24d6f-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="24d6f-116">Format</span></span>

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

### <span data-ttu-id="24d6f-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="24d6f-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="24d6f-118">A katasztrófa-helyreállítási végpontok (ha igaz) befoglalása</span><span class="sxs-lookup"><span data-stu-id="24d6f-118">Include the disaster recovery endpoints if true</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d6f-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="24d6f-119">-Name</span></span>
<span data-ttu-id="24d6f-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="24d6f-120">WebApp Name</span></span>

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

### <span data-ttu-id="24d6f-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="24d6f-121">-OutputFile</span></span>
<span data-ttu-id="24d6f-122">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="24d6f-122">Output File</span></span>

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

### <span data-ttu-id="24d6f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d6f-123">-ResourceGroupName</span></span>
<span data-ttu-id="24d6f-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="24d6f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="24d6f-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="24d6f-125">-WebApp</span></span>
<span data-ttu-id="24d6f-126">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="24d6f-126">WebApp Object</span></span>

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

### <span data-ttu-id="24d6f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d6f-127">CommonParameters</span></span>
<span data-ttu-id="24d6f-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="24d6f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d6f-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24d6f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d6f-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="24d6f-130">INPUTS</span></span>

### <span data-ttu-id="24d6f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="24d6f-131">System.String</span></span>

### <span data-ttu-id="24d6f-132">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="24d6f-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="24d6f-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="24d6f-133">OUTPUTS</span></span>

### <span data-ttu-id="24d6f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="24d6f-134">System.String</span></span>

## <span data-ttu-id="24d6f-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="24d6f-135">NOTES</span></span>

## <span data-ttu-id="24d6f-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="24d6f-136">RELATED LINKS</span></span>

[<span data-ttu-id="24d6f-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="24d6f-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="24d6f-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="24d6f-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


