---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182437"
---
# <span data-ttu-id="9a6e1-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="9a6e1-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="9a6e1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9a6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="9a6e1-103">Egy webalkalmazás pillanatképének visszaállítása</span><span class="sxs-lookup"><span data-stu-id="9a6e1-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="9a6e1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9a6e1-104">SYNTAX</span></span>

### <span data-ttu-id="9a6e1-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="9a6e1-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a6e1-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="9a6e1-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a6e1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9a6e1-107">DESCRIPTION</span></span>
<span data-ttu-id="9a6e1-108">Egy webalkalmazás pillanatképének visszaállítása a webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="9a6e1-109">A pillanatképek visszaállítása felülírja a webalkalmazások összes fájlját a pillanatképben található fájlokkal.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="9a6e1-110">Ha a beállításokat is vissza szeretné állítani, használja a RecoverConfiguration kapcsoló paramétert.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="9a6e1-111">Egy webalkalmazásról származó pillanatkép visszaállítható bármely más, ugyanazon előfizetésben lévő webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="9a6e1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="9a6e1-112">EXAMPLES</span></span>

### <span data-ttu-id="9a6e1-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9a6e1-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="9a6e1-114">A "ContosoApp" nevű webalkalmazás legújabb pillanatképét kapja meg egy, az "alapértelmezett – webes WestUS" erőforráscsoporthoz tartozó "staging" nevű bővítőhelykel.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="9a6e1-115">Visszaállítja a pillanatképet a Web App "visszaállítási" nyílásába.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="9a6e1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9a6e1-116">PARAMETERS</span></span>

### <span data-ttu-id="9a6e1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a6e1-117">-AsJob</span></span>
<span data-ttu-id="9a6e1-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="9a6e1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a6e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a6e1-119">-DefaultProfile</span></span>
<span data-ttu-id="9a6e1-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a6e1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9a6e1-121">-Force</span></span>
<span data-ttu-id="9a6e1-122">Lehetővé teszi, hogy az eredeti webalkalmazás felülírása figyelmeztetés nélkül történjen.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="9a6e1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a6e1-123">-InputObject</span></span>
<span data-ttu-id="9a6e1-124">Az Azure Web App pillanatképe.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="9a6e1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9a6e1-125">-Name</span></span>
<span data-ttu-id="9a6e1-126">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-126">The name of the web app.</span></span>

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

### <span data-ttu-id="9a6e1-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a6e1-127">-RecoverConfiguration</span></span>
<span data-ttu-id="9a6e1-128">A Web App konfigurációjának helyreállítása a fájlok mellett.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="9a6e1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a6e1-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a6e1-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a6e1-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="9a6e1-131">-Slot</span></span>
<span data-ttu-id="9a6e1-132">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="9a6e1-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="9a6e1-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="9a6e1-134">Használja az offline állapotú méretarányok pillanatképének helyreállítását.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="9a6e1-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9a6e1-135">-WebApp</span></span>
<span data-ttu-id="9a6e1-136">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="9a6e1-136">The web app object</span></span>

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

### <span data-ttu-id="9a6e1-137">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="9a6e1-137">-Confirm</span></span>
<span data-ttu-id="9a6e1-138">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a6e1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a6e1-139">-WhatIf</span></span>
<span data-ttu-id="9a6e1-140">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a6e1-141">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="9a6e1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a6e1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a6e1-142">CommonParameters</span></span>
<span data-ttu-id="9a6e1-143">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9a6e1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a6e1-144">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a6e1-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a6e1-145">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a6e1-145">INPUTS</span></span>

### <span data-ttu-id="9a6e1-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a6e1-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9a6e1-147">System. String</span><span class="sxs-lookup"><span data-stu-id="9a6e1-147">System.String</span></span>

### <span data-ttu-id="9a6e1-148">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="9a6e1-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="9a6e1-149">Microsoft. Azure. Command. WebApps. Parancsmags. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="9a6e1-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="9a6e1-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9a6e1-150">OUTPUTS</span></span>

### <span data-ttu-id="9a6e1-151">System. Void</span><span class="sxs-lookup"><span data-stu-id="9a6e1-151">System.Void</span></span>

## <span data-ttu-id="9a6e1-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9a6e1-152">NOTES</span></span>

## <span data-ttu-id="9a6e1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9a6e1-153">RELATED LINKS</span></span>
