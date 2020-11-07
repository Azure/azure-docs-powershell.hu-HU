---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: d8c25931e5eeae035f319c36698369b865500b9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842721"
---
# <span data-ttu-id="dfbe2-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="dfbe2-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="dfbe2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="dfbe2-102">SYNOPSIS</span></span>

## <span data-ttu-id="dfbe2-103">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="dfbe2-103">SYNTAX</span></span>

### <span data-ttu-id="dfbe2-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="dfbe2-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfbe2-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="dfbe2-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfbe2-106">Leírás</span><span class="sxs-lookup"><span data-stu-id="dfbe2-106">DESCRIPTION</span></span>
<span data-ttu-id="dfbe2-107">A **Remove-AzWebAppBackup** parancsmag eltávolítja az Azure Web App által megadott biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="dfbe2-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="dfbe2-108">Példák</span><span class="sxs-lookup"><span data-stu-id="dfbe2-108">EXAMPLES</span></span>

### <span data-ttu-id="dfbe2-109">1:</span><span class="sxs-lookup"><span data-stu-id="dfbe2-109">1:</span></span>
```
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="dfbe2-110">Ez a parancs eltávolítja a biztonsági másolat "12345" AZONOSÍTÓJÚ biztonsági másolatával a WebAppStandard nevű webalkalmazásból, amely az erőforráscsoport alapértelmezett – webes WestUS – tartozik.</span><span class="sxs-lookup"><span data-stu-id="dfbe2-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="dfbe2-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="dfbe2-111">PARAMETERS</span></span>

### <span data-ttu-id="dfbe2-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="dfbe2-112">-BackupId</span></span>
<span data-ttu-id="dfbe2-113">Biztonsági azonosító</span><span class="sxs-lookup"><span data-stu-id="dfbe2-113">Backup Id</span></span>

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

### <span data-ttu-id="dfbe2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbe2-114">-DefaultProfile</span></span>
<span data-ttu-id="dfbe2-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="dfbe2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfbe2-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="dfbe2-116">-Name</span></span>
<span data-ttu-id="dfbe2-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="dfbe2-117">WebApp Name</span></span>

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

### <span data-ttu-id="dfbe2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbe2-118">-ResourceGroupName</span></span>
<span data-ttu-id="dfbe2-119">Erőforráscsoporthoz tartozó név</span><span class="sxs-lookup"><span data-stu-id="dfbe2-119">Resource Group Name</span></span>

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

### <span data-ttu-id="dfbe2-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="dfbe2-120">-Slot</span></span>
<span data-ttu-id="dfbe2-121">WebApp bővítőhely neve</span><span class="sxs-lookup"><span data-stu-id="dfbe2-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="dfbe2-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dfbe2-122">-WebApp</span></span>
<span data-ttu-id="dfbe2-123">WebApp objektum</span><span class="sxs-lookup"><span data-stu-id="dfbe2-123">WebApp Object</span></span>

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

### <span data-ttu-id="dfbe2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbe2-124">CommonParameters</span></span>
<span data-ttu-id="dfbe2-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="dfbe2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbe2-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfbe2-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbe2-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfbe2-127">INPUTS</span></span>

### <span data-ttu-id="dfbe2-128">Webhely</span><span class="sxs-lookup"><span data-stu-id="dfbe2-128">Site</span></span>
<span data-ttu-id="dfbe2-129">A ' WebApp ' paraméter elfogadja a "webhely" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="dfbe2-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="dfbe2-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="dfbe2-130">OUTPUTS</span></span>

### <span data-ttu-id="dfbe2-131">Microsoft. Azure. Management. WebSites. models. BackupItem</span><span class="sxs-lookup"><span data-stu-id="dfbe2-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="dfbe2-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="dfbe2-132">NOTES</span></span>

## <span data-ttu-id="dfbe2-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="dfbe2-133">RELATED LINKS</span></span>

