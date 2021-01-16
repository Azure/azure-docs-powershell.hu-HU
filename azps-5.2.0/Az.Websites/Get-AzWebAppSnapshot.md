---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367133"
---
# <span data-ttu-id="6c21e-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="6c21e-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="6c21e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c21e-102">SYNOPSIS</span></span>
<span data-ttu-id="6c21e-103">Elérhetővé teszi a pillanatfelvételeket egy webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="6c21e-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="6c21e-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="6c21e-104">SYNTAX</span></span>

### <span data-ttu-id="6c21e-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="6c21e-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c21e-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="6c21e-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c21e-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="6c21e-107">DESCRIPTION</span></span>
<span data-ttu-id="6c21e-108">A **Get-AzWebAppSnapshot** parancsmag a webappok összes pillanatképét visszaadja.</span><span class="sxs-lookup"><span data-stu-id="6c21e-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="6c21e-109">A pillanatfelvételek a webalkalmazások fájljainak és beállításainak automatikus biztonsági mentései.</span><span class="sxs-lookup"><span data-stu-id="6c21e-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="6c21e-110">A Pillanatkép visszaállítható a **Restore-AzWebAppSnapshot** parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="6c21e-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="6c21e-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="6c21e-111">EXAMPLES</span></span>

### <span data-ttu-id="6c21e-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="6c21e-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="6c21e-113">A "ContosoApp" nevű webapp pillanatképének lekérte a "Default-Web-WestUS" erőforráscsoport "Előkészítés" nevű tárolóhelyét</span><span class="sxs-lookup"><span data-stu-id="6c21e-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="6c21e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c21e-114">PARAMETERS</span></span>

### <span data-ttu-id="6c21e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c21e-115">-DefaultProfile</span></span>
<span data-ttu-id="6c21e-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="6c21e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c21e-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6c21e-117">-Name</span></span>
<span data-ttu-id="6c21e-118">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="6c21e-118">The name of the web app.</span></span>

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

### <span data-ttu-id="6c21e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c21e-119">-ResourceGroupName</span></span>
<span data-ttu-id="6c21e-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="6c21e-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6c21e-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="6c21e-121">-Slot</span></span>
<span data-ttu-id="6c21e-122">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="6c21e-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="6c21e-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="6c21e-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="6c21e-124">Olvassa el a pillanatfelvételeket egy másodlagos méretarányú egységből.</span><span class="sxs-lookup"><span data-stu-id="6c21e-124">Read the snapshots from a secondary scale unit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c21e-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="6c21e-125">-WebApp</span></span>
<span data-ttu-id="6c21e-126">A webalkalmazás-objektum</span><span class="sxs-lookup"><span data-stu-id="6c21e-126">The web app object</span></span>

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

### <span data-ttu-id="6c21e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c21e-127">CommonParameters</span></span>
<span data-ttu-id="6c21e-128">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c21e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c21e-129">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c21e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c21e-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6c21e-130">INPUTS</span></span>

### <span data-ttu-id="6c21e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6c21e-131">System.String</span></span>

### <span data-ttu-id="6c21e-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="6c21e-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="6c21e-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="6c21e-133">OUTPUTS</span></span>

### <span data-ttu-id="6c21e-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="6c21e-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="6c21e-135">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="6c21e-135">NOTES</span></span>

## <span data-ttu-id="6c21e-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="6c21e-136">RELATED LINKS</span></span>
