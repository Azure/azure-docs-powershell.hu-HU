---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: BBC85035-DCF7-44FA-A747-A1563A55B820
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackuplist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackupList.md
ms.openlocfilehash: 6ea805f1e3a3711c2efe6faefd73edf06c4b51fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335549"
---
# <span data-ttu-id="8e81f-101">Get-AzWebAppBackupList</span><span class="sxs-lookup"><span data-stu-id="8e81f-101">Get-AzWebAppBackupList</span></span>

## <span data-ttu-id="8e81f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e81f-102">SYNOPSIS</span></span>

## <span data-ttu-id="8e81f-103">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="8e81f-103">SYNTAX</span></span>

### <span data-ttu-id="8e81f-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8e81f-104">FromResourceName</span></span>
```
Get-AzWebAppBackupList [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e81f-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8e81f-105">FromWebApp</span></span>
```
Get-AzWebAppBackupList [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e81f-106">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="8e81f-106">DESCRIPTION</span></span>
<span data-ttu-id="8e81f-107">A **Get-AzWebAppBackupList** parancsmag lekérte az Azure Web App biztonsági másolatok listáját.</span><span class="sxs-lookup"><span data-stu-id="8e81f-107">The **Get-AzWebAppBackupList** cmdlet gets a list of backups for an Azure Web App.</span></span>

## <span data-ttu-id="8e81f-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="8e81f-108">EXAMPLES</span></span>

### <span data-ttu-id="8e81f-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="8e81f-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackupList -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="8e81f-110">Ez a parancs a ContosoResourceGroup erőforráscsoporthoz társított WebApp WebAppStandardra vonatkozó biztonságimásolat-listát ad vissza.</span><span class="sxs-lookup"><span data-stu-id="8e81f-110">This command returns a backup list pertaining to WebApp WebAppStandard associated with the resource group ContosoResourceGroup.</span></span>

## <span data-ttu-id="8e81f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e81f-111">PARAMETERS</span></span>

### <span data-ttu-id="8e81f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e81f-112">-DefaultProfile</span></span>
<span data-ttu-id="8e81f-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e81f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e81f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="8e81f-114">-Name</span></span>
<span data-ttu-id="8e81f-115">WebApp neve</span><span class="sxs-lookup"><span data-stu-id="8e81f-115">WebApp Name</span></span>

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

### <span data-ttu-id="8e81f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e81f-116">-ResourceGroupName</span></span>
<span data-ttu-id="8e81f-117">Erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="8e81f-117">Resource Group Name</span></span>

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

### <span data-ttu-id="8e81f-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="8e81f-118">-Slot</span></span>
<span data-ttu-id="8e81f-119">Slot name</span><span class="sxs-lookup"><span data-stu-id="8e81f-119">Slot name</span></span>

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

### <span data-ttu-id="8e81f-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8e81f-120">-WebApp</span></span>
<span data-ttu-id="8e81f-121">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="8e81f-121">Piped WebApp</span></span>

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

### <span data-ttu-id="8e81f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e81f-122">CommonParameters</span></span>
<span data-ttu-id="8e81f-123">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e81f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e81f-124">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e81f-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e81f-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e81f-125">INPUTS</span></span>

### <span data-ttu-id="8e81f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8e81f-126">System.String</span></span>

### <span data-ttu-id="8e81f-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8e81f-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8e81f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e81f-128">OUTPUTS</span></span>

### <span data-ttu-id="8e81f-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="8e81f-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="8e81f-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="8e81f-130">NOTES</span></span>

## <span data-ttu-id="8e81f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e81f-131">RELATED LINKS</span></span>
