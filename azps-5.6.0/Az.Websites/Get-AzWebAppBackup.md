---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: 70dea111b2fc48e2d5063db21dd53a6e9ca76f75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934514"
---
# <span data-ttu-id="90795-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="90795-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="90795-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90795-102">SYNOPSIS</span></span>

## <span data-ttu-id="90795-103">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="90795-103">SYNTAX</span></span>

### <span data-ttu-id="90795-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="90795-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90795-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="90795-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90795-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="90795-106">DESCRIPTION</span></span>
<span data-ttu-id="90795-107">A **Get-AzWebAppBackup** parancsmag lekérte az Azure Web App megadott biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="90795-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="90795-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="90795-108">EXAMPLES</span></span>

### <span data-ttu-id="90795-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="90795-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="90795-110">Ez a parancs "12345" azonosítójú biztonsági másolatot kap a Default-Web-WestUS erőforráscsoporthoz tartozó WebAppStandard nevű webappból.</span><span class="sxs-lookup"><span data-stu-id="90795-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="90795-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90795-111">PARAMETERS</span></span>

### <span data-ttu-id="90795-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="90795-112">-BackupId</span></span>
<span data-ttu-id="90795-113">Biztonsági másolat azonosítója</span><span class="sxs-lookup"><span data-stu-id="90795-113">Backup Id</span></span>

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

### <span data-ttu-id="90795-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90795-114">-DefaultProfile</span></span>
<span data-ttu-id="90795-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="90795-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90795-116">-Name</span><span class="sxs-lookup"><span data-stu-id="90795-116">-Name</span></span>
<span data-ttu-id="90795-117">Webapp neve</span><span class="sxs-lookup"><span data-stu-id="90795-117">Webapp Name</span></span>

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

### <span data-ttu-id="90795-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90795-118">-ResourceGroupName</span></span>
<span data-ttu-id="90795-119">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="90795-119">Resource Group Name</span></span>

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

### <span data-ttu-id="90795-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="90795-120">-Slot</span></span>
<span data-ttu-id="90795-121">Slot Name</span><span class="sxs-lookup"><span data-stu-id="90795-121">Slot Name</span></span>

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

### <span data-ttu-id="90795-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="90795-122">-WebApp</span></span>
<span data-ttu-id="90795-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="90795-123">Piped WebApp</span></span>

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

### <span data-ttu-id="90795-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90795-124">CommonParameters</span></span>
<span data-ttu-id="90795-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90795-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90795-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90795-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90795-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90795-127">INPUTS</span></span>

### <span data-ttu-id="90795-128">System.String</span><span class="sxs-lookup"><span data-stu-id="90795-128">System.String</span></span>

### <span data-ttu-id="90795-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="90795-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="90795-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="90795-130">OUTPUTS</span></span>

### <span data-ttu-id="90795-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="90795-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="90795-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="90795-132">NOTES</span></span>

## <span data-ttu-id="90795-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="90795-133">RELATED LINKS</span></span>
