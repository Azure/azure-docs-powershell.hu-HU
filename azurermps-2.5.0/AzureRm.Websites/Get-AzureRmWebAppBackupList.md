---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackuplist
schema: 2.0.0
ms.openlocfilehash: ef409c62d56a95d36f1e7c9a02018b281c00e3c9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848614"
---
# <span data-ttu-id="f11af-101">Get-AzureRmWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="f11af-101">Get-AzureRmWebAppBackupList</span></span>

## <span data-ttu-id="f11af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f11af-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f11af-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f11af-103">SYNTAX</span></span>

### <span data-ttu-id="f11af-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f11af-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f11af-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f11af-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupList [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f11af-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="f11af-106">DESCRIPTION</span></span>
<span data-ttu-id="f11af-107">A **Get-AzureRmWebAppBackupList** parancsmag az Azure Web App biztonsági másolatainak listáját kapja.</span><span class="sxs-lookup"><span data-stu-id="f11af-107">The **Get-AzureRmWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="f11af-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f11af-108">EXAMPLES</span></span>

### <span data-ttu-id="f11af-109">1:</span><span class="sxs-lookup"><span data-stu-id="f11af-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="f11af-110">Ez a parancs visszaad egy, az erőforráscsoport ContosoResourceGroup társított WebApp WebAppStandard vonatkozó biztonsági listát.</span><span class="sxs-lookup"><span data-stu-id="f11af-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="f11af-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f11af-111">PARAMETERS</span></span>

### <span data-ttu-id="f11af-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11af-112">-DefaultProfile</span></span>
<span data-ttu-id="f11af-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f11af-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f11af-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f11af-114">-Name</span></span>
<span data-ttu-id="f11af-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="f11af-115">WebApp Name</span></span>

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

### <span data-ttu-id="f11af-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f11af-116">-ResourceGroupName</span></span>
<span data-ttu-id="f11af-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="f11af-117">Resource Group Name</span></span>

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

### <span data-ttu-id="f11af-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="f11af-118">-Slot</span></span>
<span data-ttu-id="f11af-119">Bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="f11af-119">Slot name</span></span>

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

### <span data-ttu-id="f11af-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f11af-120">-WebApp</span></span>
<span data-ttu-id="f11af-121">Vezetékes WebApp</span><span class="sxs-lookup"><span data-stu-id="f11af-121">Piped WebApp</span></span>

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

### <span data-ttu-id="f11af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11af-122">CommonParameters</span></span>
<span data-ttu-id="f11af-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f11af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11af-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f11af-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11af-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f11af-125">INPUTS</span></span>

### <span data-ttu-id="f11af-126">Webhely</span><span class="sxs-lookup"><span data-stu-id="f11af-126">Site</span></span>
<span data-ttu-id="f11af-127">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="f11af-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f11af-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f11af-128">OUTPUTS</span></span>

### <span data-ttu-id="f11af-129">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. AzureWebAppBackup []</span><span class="sxs-lookup"><span data-stu-id="f11af-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup[]</span></span>

## <span data-ttu-id="f11af-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f11af-130">NOTES</span></span>

## <span data-ttu-id="f11af-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f11af-131">RELATED LINKS</span></span>
