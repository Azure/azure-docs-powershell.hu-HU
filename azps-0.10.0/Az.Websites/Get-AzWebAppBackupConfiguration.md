---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 4c6dc810d35feedd0d0d43e0bd3b3efb7c9b6641
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842793"
---
# <span data-ttu-id="1518b-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1518b-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="1518b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1518b-102">SYNOPSIS</span></span>

## <span data-ttu-id="1518b-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1518b-103">SYNTAX</span></span>

### <span data-ttu-id="1518b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1518b-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1518b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1518b-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1518b-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="1518b-106">DESCRIPTION</span></span>
<span data-ttu-id="1518b-107">A **Get-AzWebAppBackupConfiguration** parancsmag az Azure Web App biztonsági másolatának konfigurációját kapja meg.</span><span class="sxs-lookup"><span data-stu-id="1518b-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="1518b-108">Példák</span><span class="sxs-lookup"><span data-stu-id="1518b-108">EXAMPLES</span></span>

### <span data-ttu-id="1518b-109">1:</span><span class="sxs-lookup"><span data-stu-id="1518b-109">1:</span></span>
```
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="1518b-110">Ez a parancs a WebAppStandard nevű webalkalmazás biztonsági mentési konfigurációját kapja meg, amely az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="1518b-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1518b-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1518b-111">PARAMETERS</span></span>

### <span data-ttu-id="1518b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1518b-112">-DefaultProfile</span></span>
<span data-ttu-id="1518b-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1518b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1518b-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1518b-114">-Name</span></span>
<span data-ttu-id="1518b-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="1518b-115">WebApp Name</span></span>

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

### <span data-ttu-id="1518b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1518b-116">-ResourceGroupName</span></span>
<span data-ttu-id="1518b-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="1518b-117">Resource Group Name</span></span>

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

### <span data-ttu-id="1518b-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="1518b-118">-Slot</span></span>
<span data-ttu-id="1518b-119">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="1518b-119">Slot Name</span></span>

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

### <span data-ttu-id="1518b-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1518b-120">-WebApp</span></span>
<span data-ttu-id="1518b-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="1518b-121">WebApp Name</span></span>

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

### <span data-ttu-id="1518b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1518b-122">CommonParameters</span></span>
<span data-ttu-id="1518b-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1518b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1518b-124">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1518b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1518b-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1518b-125">INPUTS</span></span>

### <span data-ttu-id="1518b-126">Webhely</span><span class="sxs-lookup"><span data-stu-id="1518b-126">Site</span></span>
<span data-ttu-id="1518b-127">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="1518b-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1518b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1518b-128">OUTPUTS</span></span>

### <span data-ttu-id="1518b-129">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1518b-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="1518b-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1518b-130">NOTES</span></span>

## <span data-ttu-id="1518b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1518b-131">RELATED LINKS</span></span>

