---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 65A78654-A490-4B60-8C16-B0CC597EE995
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppBackup.md
ms.openlocfilehash: e50c711e730f3af79ce5d8825e6beeee9b663e00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466990"
---
# <span data-ttu-id="15945-101">Remove-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="15945-101">Remove-AzWebAppBackup</span></span>

## <span data-ttu-id="15945-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15945-102">SYNOPSIS</span></span>

## <span data-ttu-id="15945-103">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="15945-103">SYNTAX</span></span>

### <span data-ttu-id="15945-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="15945-104">FromResourceName</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15945-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="15945-105">FromWebApp</span></span>
```
Remove-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15945-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="15945-106">DESCRIPTION</span></span>
<span data-ttu-id="15945-107">A **Remove-AzWebAppBackup** parancsmag eltávolítja az Azure Web App megadott biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="15945-107">The **Remove-AzWebAppBackup** cmdlet removes the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="15945-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="15945-108">EXAMPLES</span></span>

### <span data-ttu-id="15945-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="15945-109">Example 1</span></span>
```powershell
PS C:\>Remove-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="15945-110">Ez a parancs eltávolítja a biztonsági mentést "12345" azonosítójú biztonsági másolattal a Default-Web-WestUS erőforráscsoporthoz tartozó WebAppStandard nevű webappból.</span><span class="sxs-lookup"><span data-stu-id="15945-110">This command removes the backup with backup with ID of "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="15945-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15945-111">PARAMETERS</span></span>

### <span data-ttu-id="15945-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="15945-112">-BackupId</span></span>
<span data-ttu-id="15945-113">Biztonsági másolat azonosítója</span><span class="sxs-lookup"><span data-stu-id="15945-113">Backup Id</span></span>

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

### <span data-ttu-id="15945-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15945-114">-DefaultProfile</span></span>
<span data-ttu-id="15945-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15945-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15945-116">-Name</span><span class="sxs-lookup"><span data-stu-id="15945-116">-Name</span></span>
<span data-ttu-id="15945-117">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="15945-117">WebApp Name</span></span>

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

### <span data-ttu-id="15945-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15945-118">-ResourceGroupName</span></span>
<span data-ttu-id="15945-119">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="15945-119">Resource Group Name</span></span>

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

### <span data-ttu-id="15945-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="15945-120">-Slot</span></span>
<span data-ttu-id="15945-121">WebApp Slot Name</span><span class="sxs-lookup"><span data-stu-id="15945-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="15945-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="15945-122">-WebApp</span></span>
<span data-ttu-id="15945-123">WebApp-objektum</span><span class="sxs-lookup"><span data-stu-id="15945-123">WebApp Object</span></span>

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

### <span data-ttu-id="15945-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15945-124">CommonParameters</span></span>
<span data-ttu-id="15945-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15945-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15945-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15945-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15945-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15945-127">INPUTS</span></span>

### <span data-ttu-id="15945-128">System.String</span><span class="sxs-lookup"><span data-stu-id="15945-128">System.String</span></span>

### <span data-ttu-id="15945-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="15945-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="15945-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15945-130">OUTPUTS</span></span>

### <span data-ttu-id="15945-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span><span class="sxs-lookup"><span data-stu-id="15945-131">Microsoft.Azure.Management.WebSites.Models.BackupItem</span></span>

## <span data-ttu-id="15945-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="15945-132">NOTES</span></span>

## <span data-ttu-id="15945-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15945-133">RELATED LINKS</span></span>
