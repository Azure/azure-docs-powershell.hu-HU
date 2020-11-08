---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: e50c711e730f3af79ce5d8825e6beeee9b663e00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94025020"
---
# <span data-ttu-id="cfe99-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="cfe99-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="cfe99-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfe99-102">SYNOPSIS</span></span>

## <span data-ttu-id="cfe99-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfe99-103">SYNTAX</span></span>

### <span data-ttu-id="cfe99-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="cfe99-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfe99-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="cfe99-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfe99-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfe99-106">DESCRIPTION</span></span>
<span data-ttu-id="cfe99-107">A **Remove-AzWebAppBackup** parancsmag eltávolítja az Azure Web App által megadott biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="cfe99-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="cfe99-108">Példák</span><span class="sxs-lookup"><span data-stu-id="cfe99-108">EXAMPLES</span></span>

### <span data-ttu-id="cfe99-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cfe99-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="cfe99-110">Ez a parancs eltávolítja a biztonsági másolat "12345" AZONOSÍTÓJÚ biztonsági másolatával a WebAppStandard nevű webalkalmazásból, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="cfe99-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="cfe99-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfe99-111">PARAMETERS</span></span>

### <span data-ttu-id="cfe99-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="cfe99-112">-BackupId</span></span>
<span data-ttu-id="cfe99-113">Biztonsági azonosító</span><span class="sxs-lookup"><span data-stu-id="cfe99-113">Backup Id</span></span>

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

### <span data-ttu-id="cfe99-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe99-114">-DefaultProfile</span></span>
<span data-ttu-id="cfe99-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfe99-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfe99-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cfe99-116">-Name</span></span>
<span data-ttu-id="cfe99-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="cfe99-117">WebApp Name</span></span>

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

### <span data-ttu-id="cfe99-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfe99-118">-ResourceGroupName</span></span>
<span data-ttu-id="cfe99-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="cfe99-119">Resource Group Name</span></span>

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

### <span data-ttu-id="cfe99-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="cfe99-120">-Slot</span></span>
<span data-ttu-id="cfe99-121">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="cfe99-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="cfe99-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cfe99-122">-WebApp</span></span>
<span data-ttu-id="cfe99-123">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="cfe99-123">WebApp Object</span></span>

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

### <span data-ttu-id="cfe99-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe99-124">CommonParameters</span></span>
<span data-ttu-id="cfe99-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfe99-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe99-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe99-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe99-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfe99-127">INPUTS</span></span>

### <span data-ttu-id="cfe99-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe99-128">System.String</span></span>

### <span data-ttu-id="cfe99-129">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="cfe99-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cfe99-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfe99-130">OUTPUTS</span></span>

### <span data-ttu-id="cfe99-131">Microsoft. Azure. Management. WebSites. models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="cfe99-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="cfe99-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfe99-132">NOTES</span></span>

## <span data-ttu-id="cfe99-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfe99-133">RELATED LINKS</span></span>
