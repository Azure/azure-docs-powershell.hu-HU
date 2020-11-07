---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: 67bf9eb23318e4771c00760d18a5659526c5f45a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848618"
---
# <span data-ttu-id="266c6-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="266c6-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="266c6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="266c6-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="266c6-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="266c6-103">SYNTAX</span></span>

### <span data-ttu-id="266c6-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="266c6-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="266c6-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="266c6-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="266c6-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="266c6-106">DESCRIPTION</span></span>
<span data-ttu-id="266c6-107">A **Get-AzureRmWebAppBackupConfiguration** parancsmag az Azure Web App biztonsági másolatának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="266c6-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="266c6-108">Példák</span><span class="sxs-lookup"><span data-stu-id="266c6-108">EXAMPLES</span></span>

### <span data-ttu-id="266c6-109">1:</span><span class="sxs-lookup"><span data-stu-id="266c6-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="266c6-110">Ez a parancs a WebAppStandard nevű webalkalmazás biztonsági mentési konfigurációját kapja meg, amely az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="266c6-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="266c6-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="266c6-111">PARAMETERS</span></span>

### <span data-ttu-id="266c6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266c6-112">-DefaultProfile</span></span>
<span data-ttu-id="266c6-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="266c6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="266c6-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="266c6-114">-Name</span></span>
<span data-ttu-id="266c6-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="266c6-115">WebApp Name</span></span>

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

### <span data-ttu-id="266c6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="266c6-116">-ResourceGroupName</span></span>
<span data-ttu-id="266c6-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="266c6-117">Resource Group Name</span></span>

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

### <span data-ttu-id="266c6-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="266c6-118">-Slot</span></span>
<span data-ttu-id="266c6-119">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="266c6-119">Slot Name</span></span>

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

### <span data-ttu-id="266c6-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="266c6-120">-WebApp</span></span>
<span data-ttu-id="266c6-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="266c6-121">WebApp Name</span></span>

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

### <span data-ttu-id="266c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266c6-122">CommonParameters</span></span>
<span data-ttu-id="266c6-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="266c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266c6-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="266c6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266c6-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="266c6-125">INPUTS</span></span>

### <span data-ttu-id="266c6-126">Webhely</span><span class="sxs-lookup"><span data-stu-id="266c6-126">Site</span></span>
<span data-ttu-id="266c6-127">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="266c6-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="266c6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="266c6-128">OUTPUTS</span></span>

### <span data-ttu-id="266c6-129">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="266c6-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="266c6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="266c6-130">NOTES</span></span>

## <span data-ttu-id="266c6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="266c6-131">RELATED LINKS</span></span>
