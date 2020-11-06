---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: b88386077cd1a1e7b934b2a05126f00fa76bec18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499911"
---
# <span data-ttu-id="5d3b6-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="5d3b6-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="5d3b6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5d3b6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d3b6-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5d3b6-103">SYNTAX</span></span>

### <span data-ttu-id="5d3b6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5d3b6-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d3b6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5d3b6-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d3b6-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="5d3b6-106">DESCRIPTION</span></span>
<span data-ttu-id="5d3b6-107">A **Get-AzureRmWebAppBackup** parancsmag az Azure Web App megadott biztonsági másolatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="5d3b6-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="5d3b6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5d3b6-108">EXAMPLES</span></span>

### <span data-ttu-id="5d3b6-109">1:</span><span class="sxs-lookup"><span data-stu-id="5d3b6-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="5d3b6-110">Ez a parancs a "12345" azonosítójú "" azonosítójú biztonsági másolatot kapja a WebAppStandard nevű webalkalmazásban, amely az erőforráscsoport alapértelmezett – webes WestUS tartozik.</span><span class="sxs-lookup"><span data-stu-id="5d3b6-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="5d3b6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5d3b6-111">PARAMETERS</span></span>

### <span data-ttu-id="5d3b6-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="5d3b6-112">-BackupId</span></span>
<span data-ttu-id="5d3b6-113">Biztonsági azonosító</span><span class="sxs-lookup"><span data-stu-id="5d3b6-113">Backup Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3b6-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5d3b6-114">-Name</span></span>
<span data-ttu-id="5d3b6-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="5d3b6-115">Webapp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3b6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d3b6-116">-ResourceGroupName</span></span>
<span data-ttu-id="5d3b6-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="5d3b6-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3b6-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="5d3b6-118">-Slot</span></span>
<span data-ttu-id="5d3b6-119">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="5d3b6-119">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3b6-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5d3b6-120">-WebApp</span></span>
<span data-ttu-id="5d3b6-121">Vezetékes WebApp</span><span class="sxs-lookup"><span data-stu-id="5d3b6-121">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d3b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d3b6-122">-DefaultProfile</span></span>
<span data-ttu-id="5d3b6-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5d3b6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d3b6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d3b6-124">CommonParameters</span></span>
<span data-ttu-id="5d3b6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5d3b6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d3b6-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d3b6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d3b6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d3b6-127">INPUTS</span></span>

### <span data-ttu-id="5d3b6-128">Webhely</span><span class="sxs-lookup"><span data-stu-id="5d3b6-128">Site</span></span>
<span data-ttu-id="5d3b6-129">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="5d3b6-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="5d3b6-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5d3b6-130">OUTPUTS</span></span>

### <span data-ttu-id="5d3b6-131">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="5d3b6-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="5d3b6-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5d3b6-132">NOTES</span></span>

## <span data-ttu-id="5d3b6-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5d3b6-133">RELATED LINKS</span></span>

