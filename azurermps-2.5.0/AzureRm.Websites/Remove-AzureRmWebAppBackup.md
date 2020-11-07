---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: ad27e4f9f7e042fa5a649fb06131167f38f1a1be
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850210"
---
# <span data-ttu-id="caa77-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="caa77-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="caa77-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="caa77-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caa77-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="caa77-103">SYNTAX</span></span>

### <span data-ttu-id="caa77-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="caa77-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="caa77-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="caa77-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="caa77-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="caa77-106">DESCRIPTION</span></span>
<span data-ttu-id="caa77-107">A **Remove-AzureRmWebAppBackup** parancsmag eltávolítja az Azure Web App által megadott biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="caa77-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="caa77-108">Példák</span><span class="sxs-lookup"><span data-stu-id="caa77-108">EXAMPLES</span></span>

### <span data-ttu-id="caa77-109">1:</span><span class="sxs-lookup"><span data-stu-id="caa77-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="caa77-110">Ez a parancs eltávolítja a biztonsági másolat "12345" AZONOSÍTÓJÚ biztonsági másolatával a WebAppStandard nevű webalkalmazásból, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="caa77-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="caa77-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="caa77-111">PARAMETERS</span></span>

### <span data-ttu-id="caa77-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="caa77-112">-BackupId</span></span>
<span data-ttu-id="caa77-113">Biztonsági azonosító</span><span class="sxs-lookup"><span data-stu-id="caa77-113">Backup Id</span></span>

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

### <span data-ttu-id="caa77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa77-114">-DefaultProfile</span></span>
<span data-ttu-id="caa77-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="caa77-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="caa77-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="caa77-116">-Name</span></span>
<span data-ttu-id="caa77-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="caa77-117">WebApp Name</span></span>

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

### <span data-ttu-id="caa77-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caa77-118">-ResourceGroupName</span></span>
<span data-ttu-id="caa77-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="caa77-119">Resource Group Name</span></span>

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

### <span data-ttu-id="caa77-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="caa77-120">-Slot</span></span>
<span data-ttu-id="caa77-121">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="caa77-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="caa77-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="caa77-122">-WebApp</span></span>
<span data-ttu-id="caa77-123">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="caa77-123">WebApp Object</span></span>

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

### <span data-ttu-id="caa77-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa77-124">CommonParameters</span></span>
<span data-ttu-id="caa77-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="caa77-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa77-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa77-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa77-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="caa77-127">INPUTS</span></span>

### <span data-ttu-id="caa77-128">Webhely</span><span class="sxs-lookup"><span data-stu-id="caa77-128">Site</span></span>
<span data-ttu-id="caa77-129">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="caa77-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="caa77-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="caa77-130">OUTPUTS</span></span>

### <span data-ttu-id="caa77-131">Microsoft. Azure. Management. WebSites. models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="caa77-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="caa77-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="caa77-132">NOTES</span></span>

## <span data-ttu-id="caa77-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="caa77-133">RELATED LINKS</span></span>

