---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlotPublishingProfile.md
ms.openlocfilehash: 29ef83bf3ed0f423686e7ddf84bc82555bd09572
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491823"
---
# <span data-ttu-id="19b37-101">Get-AzureRmWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="19b37-101">Get-AzureRmWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="19b37-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="19b37-102">SYNOPSIS</span></span>
<span data-ttu-id="19b37-103">Beilleszt egy Azure Web App bővítőhely-közzétételi profilt.</span><span class="sxs-lookup"><span data-stu-id="19b37-103">Gets an Azure Web App slot publishing profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19b37-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="19b37-104">SYNTAX</span></span>

### <span data-ttu-id="19b37-105">S1</span><span class="sxs-lookup"><span data-stu-id="19b37-105">S1</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>] [-IncludeDisasterRecoveryEndpoints]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19b37-106">S2</span><span class="sxs-lookup"><span data-stu-id="19b37-106">S2</span></span>
```
Get-AzureRmWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="19b37-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="19b37-107">DESCRIPTION</span></span>
<span data-ttu-id="19b37-108">A **Get-AzureRmWebAppSlotPublishingProfile** parancsmag a webalkalmazás közzétételi profilját kapja meg a megadott bővítőhelyhez.</span><span class="sxs-lookup"><span data-stu-id="19b37-108">The **Get-AzureRmWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="19b37-109">Példák</span><span class="sxs-lookup"><span data-stu-id="19b37-109">EXAMPLES</span></span>

### <span data-ttu-id="19b37-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="19b37-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="19b37-111">Ez a parancs beolvassa a közzétételi profilt FTP-formátumban, amely az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp van társítva – a web-WestUS, és a megadott kimeneti fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="19b37-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="19b37-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="19b37-112">PARAMETERS</span></span>

### <span data-ttu-id="19b37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b37-113">-DefaultProfile</span></span>
<span data-ttu-id="19b37-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19b37-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19b37-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="19b37-115">-Format</span></span>
<span data-ttu-id="19b37-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="19b37-116">Format</span></span>

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

### <span data-ttu-id="19b37-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="19b37-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="19b37-118">A katasztrófa-helyreállítási végpontok (ha igaz) befoglalása</span><span class="sxs-lookup"><span data-stu-id="19b37-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="19b37-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="19b37-119">-Name</span></span>
<span data-ttu-id="19b37-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="19b37-120">WebApp Name</span></span>

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

### <span data-ttu-id="19b37-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="19b37-121">-OutputFile</span></span>
<span data-ttu-id="19b37-122">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="19b37-122">Output File</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19b37-123">-ResourceGroupName</span></span>
<span data-ttu-id="19b37-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="19b37-124">Resource Group Name</span></span>

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

### <span data-ttu-id="19b37-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="19b37-125">-Slot</span></span>
<span data-ttu-id="19b37-126">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="19b37-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="19b37-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="19b37-127">-WebApp</span></span>
<span data-ttu-id="19b37-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="19b37-128">WebApp Object</span></span>

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

### <span data-ttu-id="19b37-129">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="19b37-129">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="19b37-130">A katasztrófa-helyreállítási végpontok (ha igaz) befoglalása</span><span class="sxs-lookup"><span data-stu-id="19b37-130">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="19b37-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b37-131">CommonParameters</span></span>
<span data-ttu-id="19b37-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="19b37-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b37-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b37-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b37-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b37-134">INPUTS</span></span>

### <span data-ttu-id="19b37-135">System. String</span><span class="sxs-lookup"><span data-stu-id="19b37-135">System.String</span></span>

### <span data-ttu-id="19b37-136">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="19b37-136">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="19b37-137">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19b37-137">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="19b37-138">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19b37-138">OUTPUTS</span></span>

### <span data-ttu-id="19b37-139">System. String</span><span class="sxs-lookup"><span data-stu-id="19b37-139">System.String</span></span>

## <span data-ttu-id="19b37-140">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="19b37-140">NOTES</span></span>

## <span data-ttu-id="19b37-141">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19b37-141">RELATED LINKS</span></span>

[<span data-ttu-id="19b37-142">Reset-AzureRMWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="19b37-142">Reset-AzureRMWebAppSlotPublishingProfile</span></span>](./Reset-AzureRmWebAppSlotPublishingProfile.md)

[<span data-ttu-id="19b37-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19b37-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="19b37-144">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="19b37-144">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
