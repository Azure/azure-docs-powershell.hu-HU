---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: bd7c967bce709c1951cc7a61c1f8bfab9c78f28a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842686"
---
# <span data-ttu-id="71a75-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="71a75-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="71a75-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="71a75-102">SYNOPSIS</span></span>
<span data-ttu-id="71a75-103">Egy webalkalmazás pillanatképének visszaállítása</span><span class="sxs-lookup"><span data-stu-id="71a75-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="71a75-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="71a75-104">SYNTAX</span></span>

### <span data-ttu-id="71a75-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="71a75-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71a75-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="71a75-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71a75-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="71a75-107">DESCRIPTION</span></span>
<span data-ttu-id="71a75-108">Egy webalkalmazás pillanatképének visszaállítása a webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="71a75-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="71a75-109">A pillanatképek visszaállítása felülírja a webalkalmazások összes fájlját a pillanatképben található fájlokkal.</span><span class="sxs-lookup"><span data-stu-id="71a75-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="71a75-110">Ha a beállításokat is vissza szeretné állítani, használja a RecoverConfiguration kapcsoló paramétert.</span><span class="sxs-lookup"><span data-stu-id="71a75-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="71a75-111">Egy webalkalmazásról származó pillanatkép visszaállítható bármely más, ugyanazon előfizetésben lévő webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="71a75-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="71a75-112">Példák</span><span class="sxs-lookup"><span data-stu-id="71a75-112">EXAMPLES</span></span>

### <span data-ttu-id="71a75-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="71a75-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="71a75-114">A "ContosoApp" nevű webalkalmazás legújabb pillanatképét kapja meg egy, az "alapértelmezett – webes WestUS" erőforráscsoporthoz tartozó "staging" nevű bővítőhelykel.</span><span class="sxs-lookup"><span data-stu-id="71a75-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="71a75-115">Visszaállítja a pillanatképet a Web App "visszaállítási" nyílásába.</span><span class="sxs-lookup"><span data-stu-id="71a75-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="71a75-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="71a75-116">PARAMETERS</span></span>

### <span data-ttu-id="71a75-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71a75-117">-AsJob</span></span>
<span data-ttu-id="71a75-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="71a75-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a75-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71a75-119">-DefaultProfile</span></span>
<span data-ttu-id="71a75-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="71a75-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71a75-121">-Force</span><span class="sxs-lookup"><span data-stu-id="71a75-121">-Force</span></span>
<span data-ttu-id="71a75-122">Lehetővé teszi, hogy az eredeti webalkalmazás felülírása figyelmeztetés nélkül történjen.</span><span class="sxs-lookup"><span data-stu-id="71a75-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a75-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71a75-123">-InputObject</span></span>
<span data-ttu-id="71a75-124">Az Azure Web App pillanatképe.</span><span class="sxs-lookup"><span data-stu-id="71a75-124">The Azure Web App snapshot.</span></span>
```yaml
Type: AzureWebAppSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71a75-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="71a75-125">-Name</span></span>
<span data-ttu-id="71a75-126">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="71a75-126">The name of the web app.</span></span>
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

### <span data-ttu-id="71a75-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="71a75-127">-RecoverConfiguration</span></span>
<span data-ttu-id="71a75-128">A Web App konfigurációjának helyreállítása a fájlok mellett.</span><span class="sxs-lookup"><span data-stu-id="71a75-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71a75-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71a75-129">-ResourceGroupName</span></span>
<span data-ttu-id="71a75-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="71a75-130">The name of the resource group.</span></span>
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

### <span data-ttu-id="71a75-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="71a75-131">-Slot</span></span>
<span data-ttu-id="71a75-132">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="71a75-132">The name of the web app slot.</span></span>
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

### <span data-ttu-id="71a75-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="71a75-133">-WebApp</span></span>
<span data-ttu-id="71a75-134">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="71a75-134">The web app object</span></span>
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

### <span data-ttu-id="71a75-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="71a75-135">-Confirm</span></span>
<span data-ttu-id="71a75-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="71a75-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a75-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71a75-137">-WhatIf</span></span>
<span data-ttu-id="71a75-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="71a75-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71a75-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="71a75-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71a75-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71a75-140">CommonParameters</span></span>
<span data-ttu-id="71a75-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="71a75-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71a75-142">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71a75-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71a75-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="71a75-143">INPUTS</span></span>

### <span data-ttu-id="71a75-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="71a75-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="71a75-145">Microsoft. Azure. Management. WebSites. models. site System. String Microsoft. Azure. Command. WebApps. Parancsmags. BackupRestore. AzureWebAppSnapshot System. DateTime</span><span class="sxs-lookup"><span data-stu-id="71a75-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="71a75-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="71a75-146">OUTPUTS</span></span>

### <span data-ttu-id="71a75-147">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="71a75-147">System.Object</span></span>

## <span data-ttu-id="71a75-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="71a75-148">NOTES</span></span>

## <span data-ttu-id="71a75-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="71a75-149">RELATED LINKS</span></span>

