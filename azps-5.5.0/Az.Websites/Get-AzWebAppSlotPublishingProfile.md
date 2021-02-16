---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: B2FDB54F-0318-4037-BC1D-6113E77DDE7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslotpublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlotPublishingProfile.md
ms.openlocfilehash: 249ecef690fa4eaf59e6a7de97a75d55a285b377
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162723"
---
# <span data-ttu-id="7e9fb-101">Get-AzWebAppSlotPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="7e9fb-101">Get-AzWebAppSlotPublishingProfile</span></span>

## <span data-ttu-id="7e9fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="7e9fb-103">Egy Azure Web App-slot közzétételi profilt kap.</span><span class="sxs-lookup"><span data-stu-id="7e9fb-103">Gets an Azure Web App slot publishing profile.</span></span>

## <span data-ttu-id="7e9fb-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="7e9fb-104">SYNTAX</span></span>

### <span data-ttu-id="7e9fb-105">S1</span><span class="sxs-lookup"><span data-stu-id="7e9fb-105">S1</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e9fb-106">S2</span><span class="sxs-lookup"><span data-stu-id="7e9fb-106">S2</span></span>
```
Get-AzWebAppSlotPublishingProfile [[-OutputFile] <String>] [[-Format] <String>]
 [-IncludeDisasterRecoveryEndpoints] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e9fb-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="7e9fb-107">DESCRIPTION</span></span>
<span data-ttu-id="7e9fb-108">A **Get-AzWebAppS slotPublishingProfile** parancsmag a webapp közzétételi profilját kapja meg a megadott tárolóhelyhez.</span><span class="sxs-lookup"><span data-stu-id="7e9fb-108">The **Get-AzWebAppSlotPublishingProfile** cmdlet gets the Web App publishing profile for the specified slot.</span></span>

## <span data-ttu-id="7e9fb-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="7e9fb-109">EXAMPLES</span></span>

### <span data-ttu-id="7e9fb-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="7e9fb-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlotPublishingProfile -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "slot001" -Format "Ftp" -OutputFile "C:\Users\contoso\outputfile"
```

<span data-ttu-id="7e9fb-111">Ez a parancs Ftp formátumban jeleníti meg a Default-Web-WestUS erőforráscsoporthoz társított ContosoWebApp webapphoz tartozó slot Slot001 fájlhoz tartozó közzétételi profilt, és a megadott kimeneti fájlban tárolja.</span><span class="sxs-lookup"><span data-stu-id="7e9fb-111">This command gets the publishing profile in Ftp format for slot Slot001 pertaining to the Web App ContosoWebApp associated with the resource group Default-Web-WestUS and stores it in the specified output file.</span></span>

## <span data-ttu-id="7e9fb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e9fb-112">PARAMETERS</span></span>

### <span data-ttu-id="7e9fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e9fb-113">-DefaultProfile</span></span>
<span data-ttu-id="7e9fb-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="7e9fb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e9fb-115">-Format</span><span class="sxs-lookup"><span data-stu-id="7e9fb-115">-Format</span></span>
<span data-ttu-id="7e9fb-116">Formátum</span><span class="sxs-lookup"><span data-stu-id="7e9fb-116">Format</span></span>

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

### <span data-ttu-id="7e9fb-117">-IncludeDisasterRecoveryEndpoints</span><span class="sxs-lookup"><span data-stu-id="7e9fb-117">-IncludeDisasterRecoveryEndpoints</span></span>
<span data-ttu-id="7e9fb-118">A katasztrófa-helyreállítási végpontok beleállítása, ha igaz</span><span class="sxs-lookup"><span data-stu-id="7e9fb-118">Include the disaster recovery endpoints if true</span></span>

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

### <span data-ttu-id="7e9fb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7e9fb-119">-Name</span></span>
<span data-ttu-id="7e9fb-120">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="7e9fb-120">WebApp Name</span></span>

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

### <span data-ttu-id="7e9fb-121">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="7e9fb-121">-OutputFile</span></span>
<span data-ttu-id="7e9fb-122">Kimeneti fájl</span><span class="sxs-lookup"><span data-stu-id="7e9fb-122">Output File</span></span>

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

### <span data-ttu-id="7e9fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e9fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="7e9fb-124">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="7e9fb-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7e9fb-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="7e9fb-125">-Slot</span></span>
<span data-ttu-id="7e9fb-126">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="7e9fb-126">WebApp Slot Name</span></span>

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

### <span data-ttu-id="7e9fb-127">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7e9fb-127">-WebApp</span></span>
<span data-ttu-id="7e9fb-128">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="7e9fb-128">WebApp Object</span></span>

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

### <span data-ttu-id="7e9fb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e9fb-129">CommonParameters</span></span>
<span data-ttu-id="7e9fb-130">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e9fb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e9fb-131">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e9fb-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e9fb-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e9fb-132">INPUTS</span></span>

### <span data-ttu-id="7e9fb-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7e9fb-133">System.String</span></span>

### <span data-ttu-id="7e9fb-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="7e9fb-134">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7e9fb-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="7e9fb-135">OUTPUTS</span></span>

### <span data-ttu-id="7e9fb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7e9fb-136">System.String</span></span>

## <span data-ttu-id="7e9fb-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="7e9fb-137">NOTES</span></span>

## <span data-ttu-id="7e9fb-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="7e9fb-138">RELATED LINKS</span></span>

[<span data-ttu-id="7e9fb-139">Reset-AzWebAppSzajPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="7e9fb-139">Reset-AzWebAppSlotPublishingProfile</span></span>](./Reset-AzWebAppSlotPublishingProfile.md)

[<span data-ttu-id="7e9fb-140">Get-AzWebAppszaj</span><span class="sxs-lookup"><span data-stu-id="7e9fb-140">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="7e9fb-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7e9fb-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
