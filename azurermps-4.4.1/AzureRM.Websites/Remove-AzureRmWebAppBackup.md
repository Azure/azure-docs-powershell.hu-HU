---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppBackup.md
ms.openlocfilehash: ba7255c41b5851b1f34b2ff7a1523c691925bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504663"
---
# <span data-ttu-id="693af-101">Remove-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="693af-101">Remove-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="693af-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="693af-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="693af-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="693af-103">SYNTAX</span></span>

### <span data-ttu-id="693af-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="693af-104">FromResourceName</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="693af-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="693af-105">FromWebApp</span></span>
```
Remove-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="693af-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="693af-106">DESCRIPTION</span></span>
<span data-ttu-id="693af-107">A **Remove-AzureRmWebAppBackup** parancsmag eltávolítja az Azure Web App által megadott biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="693af-107">The **Remove-AzureRmWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="693af-108">Példák</span><span class="sxs-lookup"><span data-stu-id="693af-108">EXAMPLES</span></span>

### <span data-ttu-id="693af-109">1:</span><span class="sxs-lookup"><span data-stu-id="693af-109">1:</span></span>
```
PS C:\>Remove-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="693af-110">Ez a parancs eltávolítja a biztonsági másolat "12345" AZONOSÍTÓJÚ biztonsági másolatával a WebAppStandard nevű webalkalmazásból, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="693af-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="693af-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="693af-111">PARAMETERS</span></span>

### <span data-ttu-id="693af-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="693af-112">-BackupId</span></span>
<span data-ttu-id="693af-113">Biztonsági azonosító</span><span class="sxs-lookup"><span data-stu-id="693af-113">Backup Id</span></span>

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

### <span data-ttu-id="693af-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="693af-114">-Name</span></span>
<span data-ttu-id="693af-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="693af-115">WebApp Name</span></span>

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

### <span data-ttu-id="693af-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="693af-116">-ResourceGroupName</span></span>
<span data-ttu-id="693af-117">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="693af-117">Resource Group Name</span></span>

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

### <span data-ttu-id="693af-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="693af-118">-Slot</span></span>
<span data-ttu-id="693af-119">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="693af-119">WebApp Slot Name</span></span>

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

### <span data-ttu-id="693af-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="693af-120">-WebApp</span></span>
<span data-ttu-id="693af-121">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="693af-121">WebApp Object</span></span>

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

### <span data-ttu-id="693af-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="693af-122">-DefaultProfile</span></span>
<span data-ttu-id="693af-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="693af-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="693af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="693af-124">CommonParameters</span></span>
<span data-ttu-id="693af-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="693af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="693af-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="693af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="693af-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="693af-127">INPUTS</span></span>

### <span data-ttu-id="693af-128">Webhely</span><span class="sxs-lookup"><span data-stu-id="693af-128">Site</span></span>
<span data-ttu-id="693af-129">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="693af-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="693af-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="693af-130">OUTPUTS</span></span>

### <span data-ttu-id="693af-131">Microsoft. Azure. Management. WebSites. models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="693af-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="693af-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="693af-132">NOTES</span></span>

## <span data-ttu-id="693af-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="693af-133">RELATED LINKS</span></span>

