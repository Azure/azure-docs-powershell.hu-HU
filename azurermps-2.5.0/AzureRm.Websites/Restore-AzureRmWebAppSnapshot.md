---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 0719210cae275dc7e250e7fd14e622c51014d7c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850201"
---
# <span data-ttu-id="51011-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="51011-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="51011-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="51011-102">SYNOPSIS</span></span>
<span data-ttu-id="51011-103">Egy webalkalmazás pillanatképének visszaállítása</span><span class="sxs-lookup"><span data-stu-id="51011-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51011-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="51011-104">SYNTAX</span></span>

### <span data-ttu-id="51011-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="51011-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51011-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="51011-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="51011-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="51011-107">DESCRIPTION</span></span>
<span data-ttu-id="51011-108">Egy webalkalmazás pillanatképének visszaállítása a webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="51011-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="51011-109">A pillanatképek visszaállítása felülírja a webalkalmazások összes fájlját a pillanatképben található fájlokkal.</span><span class="sxs-lookup"><span data-stu-id="51011-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="51011-110">Ha a beállításokat is vissza szeretné állítani, használja a RecoverConfiguration kapcsoló paramétert.</span><span class="sxs-lookup"><span data-stu-id="51011-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="51011-111">Egy webalkalmazásról származó pillanatkép visszaállítható bármely más, ugyanazon előfizetésben lévő webalkalmazásra.</span><span class="sxs-lookup"><span data-stu-id="51011-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="51011-112">Példák</span><span class="sxs-lookup"><span data-stu-id="51011-112">EXAMPLES</span></span>

### <span data-ttu-id="51011-113">Példa 1</span><span class="sxs-lookup"><span data-stu-id="51011-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="51011-114">A "ContosoApp" nevű webalkalmazás legújabb pillanatképét kapja meg egy, az "alapértelmezett – webes WestUS" erőforráscsoporthoz tartozó "staging" nevű bővítőhelykel.</span><span class="sxs-lookup"><span data-stu-id="51011-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="51011-115">Visszaállítja a pillanatképet a Web App "visszaállítási" nyílásába.</span><span class="sxs-lookup"><span data-stu-id="51011-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="51011-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="51011-116">PARAMETERS</span></span>

### <span data-ttu-id="51011-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51011-117">-AsJob</span></span>
<span data-ttu-id="51011-118">A parancsmag futtatása a háttérben</span><span class="sxs-lookup"><span data-stu-id="51011-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51011-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51011-119">-DefaultProfile</span></span>
<span data-ttu-id="51011-120">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="51011-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51011-121">-Force</span><span class="sxs-lookup"><span data-stu-id="51011-121">-Force</span></span>
<span data-ttu-id="51011-122">Lehetővé teszi, hogy az eredeti webalkalmazás felülírása figyelmeztetés nélkül történjen.</span><span class="sxs-lookup"><span data-stu-id="51011-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

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

### <span data-ttu-id="51011-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51011-123">-InputObject</span></span>
<span data-ttu-id="51011-124">Az Azure Web App pillanatképe.</span><span class="sxs-lookup"><span data-stu-id="51011-124">The Azure Web App snapshot.</span></span>
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

### <span data-ttu-id="51011-125">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="51011-125">-Name</span></span>
<span data-ttu-id="51011-126">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="51011-126">The name of the web app.</span></span>
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

### <span data-ttu-id="51011-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="51011-127">-RecoverConfiguration</span></span>
<span data-ttu-id="51011-128">A Web App konfigurációjának helyreállítása a fájlok mellett.</span><span class="sxs-lookup"><span data-stu-id="51011-128">Recover the web app's configuration in addition to files.</span></span>

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

### <span data-ttu-id="51011-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51011-129">-ResourceGroupName</span></span>
<span data-ttu-id="51011-130">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="51011-130">The name of the resource group.</span></span>
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

### <span data-ttu-id="51011-131">-Slot</span><span class="sxs-lookup"><span data-stu-id="51011-131">-Slot</span></span>
<span data-ttu-id="51011-132">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="51011-132">The name of the web app slot.</span></span>
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

### <span data-ttu-id="51011-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="51011-133">-WebApp</span></span>
<span data-ttu-id="51011-134">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="51011-134">The web app object</span></span>
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

### <span data-ttu-id="51011-135">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="51011-135">-Confirm</span></span>
<span data-ttu-id="51011-136">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="51011-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51011-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51011-137">-WhatIf</span></span>
<span data-ttu-id="51011-138">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="51011-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51011-139">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="51011-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51011-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51011-140">CommonParameters</span></span>
<span data-ttu-id="51011-141">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="51011-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51011-142">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51011-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51011-143">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="51011-143">INPUTS</span></span>

### <span data-ttu-id="51011-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="51011-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="51011-145">Microsoft. Azure. Management. WebSites. models. site System. String Microsoft. Azure. Command. WebApps. Parancsmags. BackupRestore. AzureWebAppSnapshot System. DateTime</span><span class="sxs-lookup"><span data-stu-id="51011-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="51011-146">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="51011-146">OUTPUTS</span></span>

### <span data-ttu-id="51011-147">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="51011-147">System.Object</span></span>

## <span data-ttu-id="51011-148">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="51011-148">NOTES</span></span>

## <span data-ttu-id="51011-149">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="51011-149">RELATED LINKS</span></span>

