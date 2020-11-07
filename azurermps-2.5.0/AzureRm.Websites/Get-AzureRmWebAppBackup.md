---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: c6d5809211910987e06cff024d7510a70ad71a4e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848057"
---
# <span data-ttu-id="39d0f-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="39d0f-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="39d0f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="39d0f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39d0f-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="39d0f-103">SYNTAX</span></span>

### <span data-ttu-id="39d0f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="39d0f-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39d0f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="39d0f-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39d0f-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="39d0f-106">DESCRIPTION</span></span>
<span data-ttu-id="39d0f-107">A **Get-AzureRmWebAppBackup** parancsmag az Azure Web App megadott biztonsági másolatát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="39d0f-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="39d0f-108">Példák</span><span class="sxs-lookup"><span data-stu-id="39d0f-108">EXAMPLES</span></span>

### <span data-ttu-id="39d0f-109">1:</span><span class="sxs-lookup"><span data-stu-id="39d0f-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="39d0f-110">Ez a parancs a "12345" azonosítójú "" azonosítójú biztonsági másolatot kapja a WebAppStandard nevű webalkalmazásban, amely az erőforráscsoport alapértelmezett – webes WestUS tartozik.</span><span class="sxs-lookup"><span data-stu-id="39d0f-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="39d0f-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="39d0f-111">PARAMETERS</span></span>

### <span data-ttu-id="39d0f-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="39d0f-112">-BackupId</span></span>
<span data-ttu-id="39d0f-113">Biztonsági azonosító</span><span class="sxs-lookup"><span data-stu-id="39d0f-113">Backup Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39d0f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d0f-114">-DefaultProfile</span></span>
<span data-ttu-id="39d0f-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="39d0f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d0f-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="39d0f-116">-Name</span></span>
<span data-ttu-id="39d0f-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="39d0f-117">Webapp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39d0f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d0f-118">-ResourceGroupName</span></span>
<span data-ttu-id="39d0f-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="39d0f-119">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39d0f-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="39d0f-120">-Slot</span></span>
<span data-ttu-id="39d0f-121">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="39d0f-121">Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39d0f-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="39d0f-122">-WebApp</span></span>
<span data-ttu-id="39d0f-123">Vezetékes WebApp</span><span class="sxs-lookup"><span data-stu-id="39d0f-123">Piped WebApp</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39d0f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d0f-124">CommonParameters</span></span>
<span data-ttu-id="39d0f-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="39d0f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d0f-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d0f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d0f-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="39d0f-127">INPUTS</span></span>

### <span data-ttu-id="39d0f-128">Webhely</span><span class="sxs-lookup"><span data-stu-id="39d0f-128">Site</span></span>
<span data-ttu-id="39d0f-129">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="39d0f-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="39d0f-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="39d0f-130">OUTPUTS</span></span>

### <span data-ttu-id="39d0f-131">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="39d0f-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="39d0f-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="39d0f-132">NOTES</span></span>

## <span data-ttu-id="39d0f-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="39d0f-133">RELATED LINKS</span></span>

