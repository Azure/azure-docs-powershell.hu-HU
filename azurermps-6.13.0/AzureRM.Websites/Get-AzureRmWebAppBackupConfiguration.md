---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 81c9d87ecd93097c7e114a312b68d25d7dd681c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672086"
---
# <span data-ttu-id="11a90-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="11a90-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="11a90-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="11a90-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11a90-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="11a90-103">SYNTAX</span></span>

### <span data-ttu-id="11a90-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="11a90-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11a90-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="11a90-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11a90-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="11a90-106">DESCRIPTION</span></span>
<span data-ttu-id="11a90-107">A **Get-AzureRmWebAppBackupConfiguration** parancsmag az Azure Web App biztonsági másolatának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="11a90-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="11a90-108">Példák</span><span class="sxs-lookup"><span data-stu-id="11a90-108">EXAMPLES</span></span>

### <span data-ttu-id="11a90-109">1:</span><span class="sxs-lookup"><span data-stu-id="11a90-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="11a90-110">Ez a parancs a WebAppStandard nevű webalkalmazás biztonsági mentési konfigurációját kapja meg, amely az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="11a90-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="11a90-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="11a90-111">PARAMETERS</span></span>

### <span data-ttu-id="11a90-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11a90-112">-DefaultProfile</span></span>
<span data-ttu-id="11a90-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="11a90-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11a90-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="11a90-114">-Name</span></span>
<span data-ttu-id="11a90-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="11a90-115">WebApp Name</span></span>

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

### <span data-ttu-id="11a90-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11a90-116">-ResourceGroupName</span></span>
<span data-ttu-id="11a90-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="11a90-117">Resource Group Name</span></span>

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

### <span data-ttu-id="11a90-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="11a90-118">-Slot</span></span>
<span data-ttu-id="11a90-119">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="11a90-119">Slot Name</span></span>

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

### <span data-ttu-id="11a90-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="11a90-120">-WebApp</span></span>
<span data-ttu-id="11a90-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="11a90-121">WebApp Name</span></span>

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

### <span data-ttu-id="11a90-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11a90-122">CommonParameters</span></span>
<span data-ttu-id="11a90-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="11a90-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11a90-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11a90-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11a90-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="11a90-125">INPUTS</span></span>

### <span data-ttu-id="11a90-126">System. String</span><span class="sxs-lookup"><span data-stu-id="11a90-126">System.String</span></span>

### <span data-ttu-id="11a90-127">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="11a90-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="11a90-128">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="11a90-128">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="11a90-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="11a90-129">OUTPUTS</span></span>

### <span data-ttu-id="11a90-130">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="11a90-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="11a90-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="11a90-131">NOTES</span></span>

## <span data-ttu-id="11a90-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="11a90-132">RELATED LINKS</span></span>
