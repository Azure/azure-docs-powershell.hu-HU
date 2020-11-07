---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: a89ebd3142d738664cd80cab198bd6f791c1287a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668353"
---
# <span data-ttu-id="0f42e-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="0f42e-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="0f42e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f42e-102">SYNOPSIS</span></span>
<span data-ttu-id="0f42e-103">Az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="0f42e-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="0f42e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f42e-104">SYNTAX</span></span>

### <span data-ttu-id="0f42e-105">S1</span><span class="sxs-lookup"><span data-stu-id="0f42e-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f42e-106">S2</span><span class="sxs-lookup"><span data-stu-id="0f42e-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f42e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f42e-107">DESCRIPTION</span></span>
<span data-ttu-id="0f42e-108">A **Get-AzWebAppPublishingProfile** parancsmag az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="0f42e-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="0f42e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0f42e-109">EXAMPLES</span></span>

### <span data-ttu-id="0f42e-110">1:</span><span class="sxs-lookup"><span data-stu-id="0f42e-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="0f42e-111">Ez a parancs beolvassa a közzétételi profilt a webalkalmazások ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának megfelelő FTP-formátumban, a webes WestUS, és a megadott kimeneti fájlban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="0f42e-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="0f42e-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f42e-112">PARAMETERS</span></span>

### <span data-ttu-id="0f42e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f42e-113">-DefaultProfile</span></span>
<span data-ttu-id="0f42e-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f42e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f42e-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="0f42e-115">-Format</span></span>
<span data-ttu-id="0f42e-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="0f42e-116">Format</span></span>

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

### <span data-ttu-id="0f42e-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="0f42e-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="0f42e-118">A katasztrófa-helyreállítási végpontok (ha igaz) befoglalása</span><span class="sxs-lookup"><span data-stu-id="0f42e-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="0f42e-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0f42e-119">-Name</span></span>
<span data-ttu-id="0f42e-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="0f42e-120">WebApp Name</span></span>

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

### <span data-ttu-id="0f42e-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="0f42e-121">-OutputFile</span></span>
<span data-ttu-id="0f42e-122">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="0f42e-122">Output File</span></span>

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

### <span data-ttu-id="0f42e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f42e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0f42e-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="0f42e-124">Resource Group Name</span></span>

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

### <span data-ttu-id="0f42e-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="0f42e-125">-WebApp</span></span>
<span data-ttu-id="0f42e-126">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="0f42e-126">WebApp Object</span></span>

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

### <span data-ttu-id="0f42e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f42e-127">CommonParameters</span></span>
<span data-ttu-id="0f42e-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f42e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f42e-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f42e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f42e-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f42e-130">INPUTS</span></span>

### <span data-ttu-id="0f42e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0f42e-131">System.String</span></span>

### <span data-ttu-id="0f42e-132">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="0f42e-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="0f42e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f42e-133">OUTPUTS</span></span>

### <span data-ttu-id="0f42e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0f42e-134">System.String</span></span>

## <span data-ttu-id="0f42e-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f42e-135">NOTES</span></span>

## <span data-ttu-id="0f42e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f42e-136">RELATED LINKS</span></span>

[<span data-ttu-id="0f42e-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="0f42e-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="0f42e-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0f42e-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


