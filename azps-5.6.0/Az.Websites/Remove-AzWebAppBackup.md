---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: d6bba1b517f238247291af251d9f510d18029af6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940674"
---
# <span data-ttu-id="cbf0b-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="cbf0b-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="cbf0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbf0b-102">SYNOPSIS</span></span>

## <span data-ttu-id="cbf0b-103">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="cbf0b-103">SYNTAX</span></span>

### <span data-ttu-id="cbf0b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="cbf0b-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cbf0b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="cbf0b-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbf0b-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="cbf0b-106">DESCRIPTION</span></span>
<span data-ttu-id="cbf0b-107">A **Remove-AzWebAppBackup** parancsmag eltávolítja az Azure Web App megadott biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="cbf0b-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="cbf0b-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="cbf0b-108">EXAMPLES</span></span>

### <span data-ttu-id="cbf0b-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="cbf0b-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="cbf0b-110">Ez a parancs eltávolítja a biztonsági mentést "12345" azonosítójú biztonsági másolattal a Default-Web-WestUS erőforráscsoporthoz tartozó WebAppStandard nevű webappból.</span><span class="sxs-lookup"><span data-stu-id="cbf0b-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="cbf0b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbf0b-111">PARAMETERS</span></span>

### <span data-ttu-id="cbf0b-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="cbf0b-112">-BackupId</span></span>
<span data-ttu-id="cbf0b-113">Biztonsági másolat azonosítója</span><span class="sxs-lookup"><span data-stu-id="cbf0b-113">Backup Id</span></span>

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

### <span data-ttu-id="cbf0b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf0b-114">-DefaultProfile</span></span>
<span data-ttu-id="cbf0b-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cbf0b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbf0b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="cbf0b-116">-Name</span></span>
<span data-ttu-id="cbf0b-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="cbf0b-117">WebApp Name</span></span>

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

### <span data-ttu-id="cbf0b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf0b-118">-ResourceGroupName</span></span>
<span data-ttu-id="cbf0b-119">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cbf0b-119">Resource Group Name</span></span>

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

### <span data-ttu-id="cbf0b-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="cbf0b-120">-Slot</span></span>
<span data-ttu-id="cbf0b-121">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="cbf0b-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="cbf0b-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="cbf0b-122">-WebApp</span></span>
<span data-ttu-id="cbf0b-123">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="cbf0b-123">WebApp Object</span></span>

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

### <span data-ttu-id="cbf0b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf0b-124">CommonParameters</span></span>
<span data-ttu-id="cbf0b-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbf0b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf0b-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf0b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf0b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbf0b-127">INPUTS</span></span>

### <span data-ttu-id="cbf0b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="cbf0b-128">System.String</span></span>

### <span data-ttu-id="cbf0b-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="cbf0b-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="cbf0b-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cbf0b-130">OUTPUTS</span></span>

### <span data-ttu-id="cbf0b-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span><span class="sxs-lookup"><span data-stu-id="cbf0b-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="cbf0b-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="cbf0b-132">NOTES</span></span>

## <span data-ttu-id="cbf0b-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cbf0b-133">RELATED LINKS</span></span>
