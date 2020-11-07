---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 38433470-CAFD-4B8F-980C-63D4B264B39F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppPublishingProfile.md
ms.openlocfilehash: 2ba74b42225646507d5bd081300405edfb9410fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93839973"
---
# <span data-ttu-id="eea58-101">Get-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="eea58-101">Get-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="eea58-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="eea58-102">SYNOPSIS</span></span>
<span data-ttu-id="eea58-103">Az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="eea58-103">Gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="eea58-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="eea58-104">SYNTAX</span></span>

### <span data-ttu-id="eea58-105">S1</span><span class="sxs-lookup"><span data-stu-id="eea58-105">S1</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eea58-106">S2</span><span class="sxs-lookup"><span data-stu-id="eea58-106">S2</span></span>
```
Get-AzWebAppPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eea58-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="eea58-107">DESCRIPTION</span></span>
<span data-ttu-id="eea58-108">A **Get-AzWebAppPublishingProfile** parancsmag az Azure Web App közzétételi profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="eea58-108">The **Get-AzWebAppPublishingProfile** cmdlet gets an Azure Web App publishing profile.</span></span>

## <span data-ttu-id="eea58-109">Példák</span><span class="sxs-lookup"><span data-stu-id="eea58-109">EXAMPLES</span></span>

### <span data-ttu-id="eea58-110">1:</span><span class="sxs-lookup"><span data-stu-id="eea58-110">1:</span></span>
```
PS C:\> Get-AzWebAppPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile.publishsettings"
```

<span data-ttu-id="eea58-111">Ez a parancs beolvassa a közzétételi profilt a webalkalmazások ContosoWebApp társított, az erőforráscsoport alapértelmezett verziójának megfelelő FTP-formátumban, a webes WestUS, és a megadott kimeneti fájlban tárolja őket.</span><span class="sxs-lookup"><span data-stu-id="eea58-111">This command gets the publishing profile in Ftp format for Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="eea58-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="eea58-112">PARAMETERS</span></span>

### <span data-ttu-id="eea58-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea58-113">-DefaultProfile</span></span>
<span data-ttu-id="eea58-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eea58-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eea58-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="eea58-115">-Format</span></span>
<span data-ttu-id="eea58-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="eea58-116">Format</span></span>

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

### <span data-ttu-id="eea58-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="eea58-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="eea58-118">A katasztrófa-helyreállítási végpontok (ha igaz) befoglalása</span><span class="sxs-lookup"><span data-stu-id="eea58-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="eea58-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="eea58-119">-Name</span></span>
<span data-ttu-id="eea58-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="eea58-120">WebApp Name</span></span>

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

### <span data-ttu-id="eea58-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="eea58-121">-OutputFile</span></span>
<span data-ttu-id="eea58-122">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="eea58-122">Output File</span></span>

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

### <span data-ttu-id="eea58-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea58-123">-ResourceGroupName</span></span>
<span data-ttu-id="eea58-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="eea58-124">Resource Group Name</span></span>

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

### <span data-ttu-id="eea58-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="eea58-125">-WebApp</span></span>
<span data-ttu-id="eea58-126">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="eea58-126">WebApp Object</span></span>

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

### <span data-ttu-id="eea58-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea58-127">CommonParameters</span></span>
<span data-ttu-id="eea58-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="eea58-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea58-129">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea58-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea58-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="eea58-130">INPUTS</span></span>

### <span data-ttu-id="eea58-131">System. String</span><span class="sxs-lookup"><span data-stu-id="eea58-131">System.String</span></span>

### <span data-ttu-id="eea58-132">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="eea58-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="eea58-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eea58-133">OUTPUTS</span></span>

### <span data-ttu-id="eea58-134">System. String</span><span class="sxs-lookup"><span data-stu-id="eea58-134">System.String</span></span>

## <span data-ttu-id="eea58-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="eea58-135">NOTES</span></span>

## <span data-ttu-id="eea58-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eea58-136">RELATED LINKS</span></span>

[<span data-ttu-id="eea58-137">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="eea58-137">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="eea58-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="eea58-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


