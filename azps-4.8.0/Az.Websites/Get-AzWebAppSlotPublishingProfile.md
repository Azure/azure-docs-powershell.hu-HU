---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183435"
---
# <span data-ttu-id="546ac-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="546ac-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="546ac-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="546ac-102">SYNOPSIS</span></span>
<span data-ttu-id="546ac-103">Beilleszt egy Azure Web App bővítőhely-közzétételi profilt.</span><span class="sxs-lookup"><span data-stu-id="546ac-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="546ac-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="546ac-104">SYNTAX</span></span>

### <span data-ttu-id="546ac-105">S1</span><span class="sxs-lookup"><span data-stu-id="546ac-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546ac-106">S2</span><span class="sxs-lookup"><span data-stu-id="546ac-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="546ac-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="546ac-107">DESCRIPTION</span></span>
<span data-ttu-id="546ac-108">A **Get-AzWebAppSlotPublishingProfile** parancsmag a webalkalmazás közzétételi profilját kapja meg a megadott bővítőhelyhez.</span><span class="sxs-lookup"><span data-stu-id="546ac-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="546ac-109">Példák</span><span class="sxs-lookup"><span data-stu-id="546ac-109">EXAMPLES</span></span>

### <span data-ttu-id="546ac-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="546ac-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="546ac-111">Ez a parancs beolvassa a közzétételi profilt FTP-formátumban, amely az erőforráscsoport alapértelmezett Slot001 tartozó webalkalmazás-ContosoWebApp van társítva – a web-WestUS, és a megadott kimeneti fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="546ac-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="546ac-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="546ac-112">PARAMETERS</span></span>

### <span data-ttu-id="546ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546ac-113">-DefaultProfile</span></span>
<span data-ttu-id="546ac-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="546ac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="546ac-115">Formátumú</span><span class="sxs-lookup"><span data-stu-id="546ac-115">-Format</span></span>
<span data-ttu-id="546ac-116">Formázása</span><span class="sxs-lookup"><span data-stu-id="546ac-116">Format</span></span>

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

### <span data-ttu-id="546ac-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="546ac-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="546ac-118">A katasztrófa-helyreállítási végpontok (ha igaz) befoglalása</span><span class="sxs-lookup"><span data-stu-id="546ac-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="546ac-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="546ac-119">-Name</span></span>
<span data-ttu-id="546ac-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="546ac-120">WebApp Name</span></span>

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

### <span data-ttu-id="546ac-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="546ac-121">-OutputFile</span></span>
<span data-ttu-id="546ac-122">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="546ac-122">Output File</span></span>

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

### <span data-ttu-id="546ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="546ac-124">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="546ac-124">Resource Group Name</span></span>

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

### <span data-ttu-id="546ac-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="546ac-125">-Slot</span></span>
<span data-ttu-id="546ac-126">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="546ac-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="546ac-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="546ac-127">-WebApp</span></span>
<span data-ttu-id="546ac-128">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="546ac-128">WebApp Object</span></span>

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

### <span data-ttu-id="546ac-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546ac-129">CommonParameters</span></span>
<span data-ttu-id="546ac-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="546ac-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546ac-131">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="546ac-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546ac-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="546ac-132">INPUTS</span></span>

### <span data-ttu-id="546ac-133">System. String</span><span class="sxs-lookup"><span data-stu-id="546ac-133">System.String</span></span>

### <span data-ttu-id="546ac-134">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="546ac-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="546ac-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="546ac-135">OUTPUTS</span></span>

### <span data-ttu-id="546ac-136">System. String</span><span class="sxs-lookup"><span data-stu-id="546ac-136">System.String</span></span>

## <span data-ttu-id="546ac-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="546ac-137">NOTES</span></span>

## <span data-ttu-id="546ac-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="546ac-138">RELATED LINKS</span></span>

[<span data-ttu-id="546ac-139">Reset-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="546ac-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="546ac-140">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="546ac-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="546ac-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="546ac-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
