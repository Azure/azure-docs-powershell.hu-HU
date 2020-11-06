---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 536d0fe0f32231bfd732698c584e02be95d5c20e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494843"
---
# <span data-ttu-id="4bbf1-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4bbf1-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="4bbf1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4bbf1-102">SYNOPSIS</span></span>
<span data-ttu-id="4bbf1-103">Egy webalkalmazás pillanatképének visszaállítása</span><span class="sxs-lookup"><span data-stu-id="4bbf1-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bbf1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4bbf1-104">SYNTAX</span></span>

### <span data-ttu-id="4bbf1-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4bbf1-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bbf1-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4bbf1-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bbf1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4bbf1-107">DESCRIPTION</span></span>
<span data-ttu-id="4bbf1-108">Egy webalkalmazás pillanatképének visszaállítása a webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="4bbf1-109">A pillanatképek visszaállítása felülírja a webalkalmazások összes fájlját a pillanatképben található fájlokkal.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="4bbf1-110">Ha a beállításokat is vissza szeretné állítani, használja a RecoverConfiguration kapcsoló paramétert.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="4bbf1-111">Egy webalkalmazásról származó pillanatkép visszaállítható bármely más, ugyanazon előfizetésben lévő webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="4bbf1-112">Példák</span><span class="sxs-lookup"><span data-stu-id="4bbf1-112">EXAMPLES</span></span>

### <span data-ttu-id="4bbf1-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4bbf1-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="4bbf1-114">A "ContosoApp" nevű webalkalmazás legújabb pillanatképét kapja meg egy, az "alapértelmezett – webes WestUS" erőforráscsoporthoz tartozó "staging" nevű bővítőhelykel.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="4bbf1-115">Visszaállítja a pillanatképet a Web App "visszaállítási" nyílásába.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="4bbf1-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4bbf1-116">PARAMETERS</span></span>

### <span data-ttu-id="4bbf1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4bbf1-117">-AsJob</span></span>
<span data-ttu-id="4bbf1-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="4bbf1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4bbf1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bbf1-119">-DefaultProfile</span></span>
<span data-ttu-id="4bbf1-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bbf1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4bbf1-121">-Force</span></span>
<span data-ttu-id="4bbf1-122">Lehetővé teszi, hogy az eredeti webalkalmazás felülírása figyelmeztetés nélkül történjen.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="4bbf1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bbf1-123">-InputObject</span></span>
<span data-ttu-id="4bbf1-124">Az Azure Web App pillanatképe.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-124">The Azure Web App snapshot.</span></span>

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

### <span data-ttu-id="4bbf1-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4bbf1-125">-Name</span></span>
<span data-ttu-id="4bbf1-126">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-126">The name of the web app.</span></span>

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

### <span data-ttu-id="4bbf1-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="4bbf1-127">-RecoverConfiguration</span></span>
<span data-ttu-id="4bbf1-128">A Web App konfigurációjának helyreállítása a fájlok mellett.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="4bbf1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bbf1-129">-ResourceGroupName</span></span>
<span data-ttu-id="4bbf1-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="4bbf1-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="4bbf1-131">-Slot</span></span>
<span data-ttu-id="4bbf1-132">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-132">The name of the web app slot.</span></span>

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

### <span data-ttu-id="4bbf1-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4bbf1-133">-WebApp</span></span>
<span data-ttu-id="4bbf1-134">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="4bbf1-134">The web app object</span></span>

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

### <span data-ttu-id="4bbf1-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="4bbf1-135">-Confirm</span></span>
<span data-ttu-id="4bbf1-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bbf1-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bbf1-137">-WhatIf</span></span>
<span data-ttu-id="4bbf1-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bbf1-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="4bbf1-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bbf1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bbf1-140">CommonParameters</span></span>
<span data-ttu-id="4bbf1-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4bbf1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bbf1-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bbf1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bbf1-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bbf1-143">INPUTS</span></span>

### <span data-ttu-id="4bbf1-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4bbf1-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4bbf1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4bbf1-145">System.String</span></span>

### <span data-ttu-id="4bbf1-146">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="4bbf1-146">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="4bbf1-147">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4bbf1-147">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="4bbf1-148">Microsoft. Azure. Command. WebApps. Parancsmags. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4bbf1-148">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>
<span data-ttu-id="4bbf1-149">Paraméterek: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4bbf1-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4bbf1-150">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4bbf1-150">OUTPUTS</span></span>

### <span data-ttu-id="4bbf1-151">System. Void</span><span class="sxs-lookup"><span data-stu-id="4bbf1-151">System.Void</span></span>

## <span data-ttu-id="4bbf1-152">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4bbf1-152">NOTES</span></span>

## <span data-ttu-id="4bbf1-153">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4bbf1-153">RELATED LINKS</span></span>
