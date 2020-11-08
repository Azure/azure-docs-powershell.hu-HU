---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187124"
---
# <span data-ttu-id="5e6b2-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="5e6b2-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="5e6b2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5e6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="5e6b2-103">Elérhetővé válik a webes alkalmazások számára elérhető Pillanatképek.</span><span class="sxs-lookup"><span data-stu-id="5e6b2-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="5e6b2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5e6b2-104">SYNTAX</span></span>

### <span data-ttu-id="5e6b2-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="5e6b2-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e6b2-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="5e6b2-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e6b2-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="5e6b2-107">DESCRIPTION</span></span>
<span data-ttu-id="5e6b2-108">A **Get-AzWebAppSnapshot** parancsmag minden pillanatképet visszaadott egy webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="5e6b2-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="5e6b2-109">A pillanatképek automatikusan biztonsági másolatot készítenek egy webalkalmazás fájljairól és beállításairól.</span><span class="sxs-lookup"><span data-stu-id="5e6b2-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="5e6b2-110">Egy pillanatkép visszaállítható a **Restore-AzWebAppSnapshot** parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="5e6b2-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="5e6b2-111">Példák</span><span class="sxs-lookup"><span data-stu-id="5e6b2-111">EXAMPLES</span></span>

### <span data-ttu-id="5e6b2-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5e6b2-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="5e6b2-113">A "ContosoApp" nevű webalkalmazás pillanatfelvételének beszerzése a "Default-Web-WestUS" erőforráscsoporthoz tartozó "staging" nevű bővítőhelykel</span><span class="sxs-lookup"><span data-stu-id="5e6b2-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="5e6b2-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5e6b2-114">PARAMETERS</span></span>

### <span data-ttu-id="5e6b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e6b2-115">-DefaultProfile</span></span>
<span data-ttu-id="5e6b2-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5e6b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e6b2-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5e6b2-117">-Name</span></span>
<span data-ttu-id="5e6b2-118">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="5e6b2-118">The name of the web app.</span></span>

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

### <span data-ttu-id="5e6b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e6b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e6b2-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5e6b2-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e6b2-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="5e6b2-121">-Slot</span></span>
<span data-ttu-id="5e6b2-122">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="5e6b2-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="5e6b2-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="5e6b2-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="5e6b2-124">Olvassa el a másodlagos méretarányokból származó Pillanatképek című témakört.</span><span class="sxs-lookup"><span data-stu-id="5e6b2-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="5e6b2-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5e6b2-125">-WebApp</span></span>
<span data-ttu-id="5e6b2-126">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="5e6b2-126">The web app object</span></span>

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

### <span data-ttu-id="5e6b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e6b2-127">CommonParameters</span></span>
<span data-ttu-id="5e6b2-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5e6b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e6b2-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e6b2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e6b2-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e6b2-130">INPUTS</span></span>

### <span data-ttu-id="5e6b2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5e6b2-131">System.String</span></span>

### <span data-ttu-id="5e6b2-132">Microsoft. Azure. Command. WebApps. models. PSSite</span><span class="sxs-lookup"><span data-stu-id="5e6b2-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5e6b2-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5e6b2-133">OUTPUTS</span></span>

### <span data-ttu-id="5e6b2-134">Microsoft. Azure. Command. WebApps. Parancsmags. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="5e6b2-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="5e6b2-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5e6b2-135">NOTES</span></span>

## <span data-ttu-id="5e6b2-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5e6b2-136">RELATED LINKS</span></span>
