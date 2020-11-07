---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: 7b3e721adaa0389f1c2a75750d7bf36dfe4c2ac1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93671951"
---
# <span data-ttu-id="6e084-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6e084-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="6e084-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="6e084-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e084-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="6e084-103">SYNTAX</span></span>

### <span data-ttu-id="6e084-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6e084-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e084-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6e084-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e084-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="6e084-106">DESCRIPTION</span></span>
<span data-ttu-id="6e084-107">A **Get-AzureRmWebAppBackup** parancsmag az Azure Web App megadott biztonsági másolatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="6e084-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="6e084-108">Példák</span><span class="sxs-lookup"><span data-stu-id="6e084-108">EXAMPLES</span></span>

### <span data-ttu-id="6e084-109">1:</span><span class="sxs-lookup"><span data-stu-id="6e084-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="6e084-110">Ez a parancs a "12345" azonosítójú "" azonosítójú biztonsági másolatot kapja a WebAppStandard nevű webalkalmazásban, amely az erőforráscsoport alapértelmezett – webes WestUS tartozik.</span><span class="sxs-lookup"><span data-stu-id="6e084-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="6e084-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="6e084-111">PARAMETERS</span></span>

### <span data-ttu-id="6e084-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="6e084-112">-BackupId</span></span>
<span data-ttu-id="6e084-113">Biztonsági azonosító</span><span class="sxs-lookup"><span data-stu-id="6e084-113">Backup Id</span></span>

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

### <span data-ttu-id="6e084-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e084-114">-DefaultProfile</span></span>
<span data-ttu-id="6e084-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6e084-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e084-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="6e084-116">-Name</span></span>
<span data-ttu-id="6e084-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="6e084-117">Webapp Name</span></span>

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

### <span data-ttu-id="6e084-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e084-118">-ResourceGroupName</span></span>
<span data-ttu-id="6e084-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="6e084-119">Resource Group Name</span></span>

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

### <span data-ttu-id="6e084-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="6e084-120">-Slot</span></span>
<span data-ttu-id="6e084-121">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="6e084-121">Slot Name</span></span>

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

### <span data-ttu-id="6e084-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6e084-122">-WebApp</span></span>
<span data-ttu-id="6e084-123">Vezetékes WebApp</span><span class="sxs-lookup"><span data-stu-id="6e084-123">Piped WebApp</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e084-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e084-124">CommonParameters</span></span>
<span data-ttu-id="6e084-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="6e084-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e084-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e084-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e084-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e084-127">INPUTS</span></span>

### <span data-ttu-id="6e084-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6e084-128">System.String</span></span>

### <span data-ttu-id="6e084-129">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="6e084-129">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="6e084-130">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e084-130">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="6e084-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6e084-131">OUTPUTS</span></span>

### <span data-ttu-id="6e084-132">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="6e084-132">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="6e084-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="6e084-133">NOTES</span></span>

## <span data-ttu-id="6e084-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6e084-134">RELATED LINKS</span></span>
