---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 30f1581ddd4668fbe4d4d4b6d8c902f6aac929ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668363"
---
# <span data-ttu-id="23816-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="23816-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="23816-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="23816-102">SYNOPSIS</span></span>

## <span data-ttu-id="23816-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="23816-103">SYNTAX</span></span>

### <span data-ttu-id="23816-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="23816-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23816-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="23816-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23816-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="23816-106">DESCRIPTION</span></span>
<span data-ttu-id="23816-107">A **Get-AzWebAppBackup** parancsmag az Azure Web App megadott biztonsági másolatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="23816-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="23816-108">Példák</span><span class="sxs-lookup"><span data-stu-id="23816-108">EXAMPLES</span></span>

### <span data-ttu-id="23816-109">1:</span><span class="sxs-lookup"><span data-stu-id="23816-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="23816-110">Ez a parancs a "12345" azonosítójú "" azonosítójú biztonsági másolatot kapja a WebAppStandard nevű webalkalmazásban, amely az erőforráscsoport alapértelmezett – webes WestUS tartozik.</span><span class="sxs-lookup"><span data-stu-id="23816-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="23816-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="23816-111">PARAMETERS</span></span>

### <span data-ttu-id="23816-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="23816-112">-BackupId</span></span>
<span data-ttu-id="23816-113">Biztonsági azonosító</span><span class="sxs-lookup"><span data-stu-id="23816-113">Backup Id</span></span>

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

### <span data-ttu-id="23816-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23816-114">-DefaultProfile</span></span>
<span data-ttu-id="23816-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="23816-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23816-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="23816-116">-Name</span></span>
<span data-ttu-id="23816-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="23816-117">Webapp Name</span></span>

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

### <span data-ttu-id="23816-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23816-118">-ResourceGroupName</span></span>
<span data-ttu-id="23816-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="23816-119">Resource Group Name</span></span>

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

### <span data-ttu-id="23816-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="23816-120">-Slot</span></span>
<span data-ttu-id="23816-121">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="23816-121">Slot Name</span></span>

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

### <span data-ttu-id="23816-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="23816-122">-WebApp</span></span>
<span data-ttu-id="23816-123">Vezetékes WebApp</span><span class="sxs-lookup"><span data-stu-id="23816-123">Piped WebApp</span></span>

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

### <span data-ttu-id="23816-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23816-124">CommonParameters</span></span>
<span data-ttu-id="23816-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="23816-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23816-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23816-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23816-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="23816-127">INPUTS</span></span>

### <span data-ttu-id="23816-128">System. String</span><span class="sxs-lookup"><span data-stu-id="23816-128">System.String</span></span>

### <span data-ttu-id="23816-129">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="23816-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="23816-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="23816-130">OUTPUTS</span></span>

### <span data-ttu-id="23816-131">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="23816-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="23816-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="23816-132">NOTES</span></span>

## <span data-ttu-id="23816-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="23816-133">RELATED LINKS</span></span>
