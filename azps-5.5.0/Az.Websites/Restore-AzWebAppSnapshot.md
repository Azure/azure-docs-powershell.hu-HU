---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149658"
---
# <span data-ttu-id="341cf-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="341cf-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="341cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="341cf-102">SYNOPSIS</span></span>
<span data-ttu-id="341cf-103">Webalkalmazás pillanatképének visszaállítása.</span><span class="sxs-lookup"><span data-stu-id="341cf-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="341cf-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="341cf-104">SYNTAX</span></span>

### <span data-ttu-id="341cf-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="341cf-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="341cf-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="341cf-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="341cf-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="341cf-107">DESCRIPTION</span></span>
<span data-ttu-id="341cf-108">Visszaállítja a webalkalmazás pillanatképét a webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="341cf-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="341cf-109">A pillanatkép visszaállítása felülírja a webalkalmazás összes fájlját a pillanatfelvételben lévő fájlokkal.</span><span class="sxs-lookup"><span data-stu-id="341cf-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="341cf-110">A beállítások visszaállításához használja a RecoverConfiguration kapcsoló paramétert.</span><span class="sxs-lookup"><span data-stu-id="341cf-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="341cf-111">Az egyik webalkalmazás pillanatfelvétele visszaállítható az adott előfizetés bármely másik webalkalmazására.</span><span class="sxs-lookup"><span data-stu-id="341cf-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="341cf-112">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="341cf-112">EXAMPLES</span></span>

### <span data-ttu-id="341cf-113">1. példa</span><span class="sxs-lookup"><span data-stu-id="341cf-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="341cf-114">A "ContosoApp" nevű webapp legújabb pillanatképét kapja a "Default-Web-WestUS" erőforráscsoport "Előkészítés" nevű tárolóhelyét használva.</span><span class="sxs-lookup"><span data-stu-id="341cf-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="341cf-115">Visszaállítja a pillanatfelvételt a webalkalmazás "Visszaállítás" tárolóhelyéhez.</span><span class="sxs-lookup"><span data-stu-id="341cf-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="341cf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="341cf-116">PARAMETERS</span></span>

### <span data-ttu-id="341cf-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="341cf-117">-AsJob</span></span>
<span data-ttu-id="341cf-118">Parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="341cf-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="341cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="341cf-119">-DefaultProfile</span></span>
<span data-ttu-id="341cf-120">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="341cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="341cf-121">-Force</span><span class="sxs-lookup"><span data-stu-id="341cf-121">-Force</span></span>
<span data-ttu-id="341cf-122">Lehetővé teszi az eredeti webalkalmazás felülírését figyelmeztetés megjelenítése nélkül.</span><span class="sxs-lookup"><span data-stu-id="341cf-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="341cf-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="341cf-123">-InputObject</span></span>
<span data-ttu-id="341cf-124">Az Azure Web App pillanatképe.</span><span class="sxs-lookup"><span data-stu-id="341cf-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="341cf-125">-Name</span><span class="sxs-lookup"><span data-stu-id="341cf-125">-Name</span></span>
<span data-ttu-id="341cf-126">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="341cf-126">The name of the web app.</span></span>

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

### <span data-ttu-id="341cf-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="341cf-127">-RecoverConfiguration</span></span>
<span data-ttu-id="341cf-128">A fájlokon kívül a webalkalmazás konfigurációját is helyreállítja.</span><span class="sxs-lookup"><span data-stu-id="341cf-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="341cf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="341cf-129">-ResourceGroupName</span></span>
<span data-ttu-id="341cf-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="341cf-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="341cf-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="341cf-131">-Slot</span></span>
<span data-ttu-id="341cf-132">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="341cf-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="341cf-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="341cf-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="341cf-134">Kapcsolat nélküli méretarányú egység pillanatképének helyreállítására használható.</span><span class="sxs-lookup"><span data-stu-id="341cf-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="341cf-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="341cf-135">-WebApp</span></span>
<span data-ttu-id="341cf-136">A webalkalmazás-objektum</span><span class="sxs-lookup"><span data-stu-id="341cf-136">The web app object</span></span>

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

### <span data-ttu-id="341cf-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="341cf-137">-Confirm</span></span>
<span data-ttu-id="341cf-138">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="341cf-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341cf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="341cf-139">-WhatIf</span></span>
<span data-ttu-id="341cf-140">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="341cf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="341cf-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="341cf-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="341cf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341cf-142">CommonParameters</span></span>
<span data-ttu-id="341cf-143">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="341cf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="341cf-144">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="341cf-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341cf-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="341cf-145">INPUTS</span></span>

### <span data-ttu-id="341cf-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="341cf-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="341cf-147">System.String</span><span class="sxs-lookup"><span data-stu-id="341cf-147">System.String</span></span>

### <span data-ttu-id="341cf-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="341cf-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="341cf-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="341cf-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="341cf-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="341cf-150">OUTPUTS</span></span>

### <span data-ttu-id="341cf-151">System.Void</span><span class="sxs-lookup"><span data-stu-id="341cf-151">System.Void</span></span>

## <span data-ttu-id="341cf-152">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="341cf-152">NOTES</span></span>

## <span data-ttu-id="341cf-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="341cf-153">RELATED LINKS</span></span>
