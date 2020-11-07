---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 426fc5c6cac67da7b0380b3a5e5e40cc1b533366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93673072"
---
# <span data-ttu-id="8b260-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b260-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="8b260-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8b260-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b260-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8b260-103">SYNTAX</span></span>

### <span data-ttu-id="8b260-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8b260-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b260-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8b260-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b260-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="8b260-106">DESCRIPTION</span></span>
<span data-ttu-id="8b260-107">A **Get-AzureRmWebAppBackupConfiguration** parancsmag az Azure Web App biztonsági másolatának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8b260-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="8b260-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8b260-108">EXAMPLES</span></span>

### <span data-ttu-id="8b260-109">1:</span><span class="sxs-lookup"><span data-stu-id="8b260-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="8b260-110">Ez a parancs a WebAppStandard nevű webalkalmazás biztonsági mentési konfigurációját kapja meg, amely az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8b260-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="8b260-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8b260-111">PARAMETERS</span></span>

### <span data-ttu-id="8b260-112">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="8b260-112">-Name</span></span>
<span data-ttu-id="8b260-113">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="8b260-113">WebApp Name</span></span>

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

### <span data-ttu-id="8b260-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b260-114">-ResourceGroupName</span></span>
<span data-ttu-id="8b260-115">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="8b260-115">Resource Group Name</span></span>

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

### <span data-ttu-id="8b260-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="8b260-116">-Slot</span></span>
<span data-ttu-id="8b260-117">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="8b260-117">Slot Name</span></span>

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

### <span data-ttu-id="8b260-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8b260-118">-WebApp</span></span>
<span data-ttu-id="8b260-119">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="8b260-119">WebApp Name</span></span>

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

### <span data-ttu-id="8b260-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b260-120">-DefaultProfile</span></span>
<span data-ttu-id="8b260-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8b260-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b260-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b260-122">CommonParameters</span></span>
<span data-ttu-id="8b260-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8b260-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b260-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b260-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b260-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b260-125">INPUTS</span></span>

### <span data-ttu-id="8b260-126">Webhely</span><span class="sxs-lookup"><span data-stu-id="8b260-126">Site</span></span>
<span data-ttu-id="8b260-127">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8b260-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8b260-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8b260-128">OUTPUTS</span></span>

### <span data-ttu-id="8b260-129">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="8b260-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="8b260-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8b260-130">NOTES</span></span>

## <span data-ttu-id="8b260-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8b260-131">RELATED LINKS</span></span>

