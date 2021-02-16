---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupConfiguration.md
ms.openlocfilehash: 8ef8639c2ff79a326a8d0ffcdf1f1dca24dbccf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208879"
---
# <span data-ttu-id="d5ec3-101">Get-AzWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5ec3-101">Get-AzWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d5ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5ec3-102">SYNOPSIS</span></span>

## <span data-ttu-id="d5ec3-103">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d5ec3-103">SYNTAX</span></span>

### <span data-ttu-id="d5ec3-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d5ec3-104">FromResourceName</span></span>
```
Get-AzWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5ec3-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d5ec3-105">FromWebApp</span></span>
```
Get-AzWebAppBackupConfiguration [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5ec3-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d5ec3-106">DESCRIPTION</span></span>
<span data-ttu-id="d5ec3-107">A **Get-AzWebAppBackupConfiguration** parancsmag lekérte az Azure Web App biztonsági másolatát.</span><span class="sxs-lookup"><span data-stu-id="d5ec3-107">The **Get-AzWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="d5ec3-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d5ec3-108">EXAMPLES</span></span>

### <span data-ttu-id="d5ec3-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="d5ec3-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="d5ec3-110">Ez a parancs a Biztonsági másolat típusú konfigurációt a Default-Web-WestUS erőforráscsoport WebAppStandard nevű webappjában kapja meg.</span><span class="sxs-lookup"><span data-stu-id="d5ec3-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="d5ec3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5ec3-111">PARAMETERS</span></span>

### <span data-ttu-id="d5ec3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ec3-112">-DefaultProfile</span></span>
<span data-ttu-id="d5ec3-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d5ec3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5ec3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="d5ec3-114">-Name</span></span>
<span data-ttu-id="d5ec3-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="d5ec3-115">WebApp Name</span></span>

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

### <span data-ttu-id="d5ec3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ec3-116">-ResourceGroupName</span></span>
<span data-ttu-id="d5ec3-117">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="d5ec3-117">Resource Group Name</span></span>

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

### <span data-ttu-id="d5ec3-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="d5ec3-118">-Slot</span></span>
<span data-ttu-id="d5ec3-119">Slot Name</span><span class="sxs-lookup"><span data-stu-id="d5ec3-119">Slot Name</span></span>

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

### <span data-ttu-id="d5ec3-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="d5ec3-120">-WebApp</span></span>
<span data-ttu-id="d5ec3-121">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="d5ec3-121">WebApp Name</span></span>

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

### <span data-ttu-id="d5ec3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ec3-122">CommonParameters</span></span>
<span data-ttu-id="d5ec3-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ec3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ec3-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ec3-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ec3-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5ec3-125">INPUTS</span></span>

### <span data-ttu-id="d5ec3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d5ec3-126">System.String</span></span>

### <span data-ttu-id="d5ec3-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="d5ec3-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="d5ec3-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5ec3-128">OUTPUTS</span></span>

### <span data-ttu-id="d5ec3-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d5ec3-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="d5ec3-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d5ec3-130">NOTES</span></span>

## <span data-ttu-id="d5ec3-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5ec3-131">RELATED LINKS</span></span>
