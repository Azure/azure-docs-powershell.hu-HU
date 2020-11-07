---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848373"
---
# <span data-ttu-id="72039-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="72039-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="72039-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="72039-102">SYNOPSIS</span></span>
<span data-ttu-id="72039-103">Elérhetővé válik a webes alkalmazások számára elérhető Pillanatképek.</span><span class="sxs-lookup"><span data-stu-id="72039-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72039-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="72039-104">SYNTAX</span></span>

### <span data-ttu-id="72039-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="72039-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="72039-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="72039-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="72039-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="72039-107">DESCRIPTION</span></span>
<span data-ttu-id="72039-108">A **Get-AzureRmWebAppSnapshot** parancsmag minden pillanatképet visszaadott egy webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="72039-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="72039-109">A pillanatképek automatikusan biztonsági másolatot készítenek egy webalkalmazás fájljairól és beállításairól.</span><span class="sxs-lookup"><span data-stu-id="72039-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="72039-110">Egy pillanatkép visszaállítható a **Restore-AzureRmWebAppSnapshot** parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="72039-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="72039-111">Példák</span><span class="sxs-lookup"><span data-stu-id="72039-111">EXAMPLES</span></span>

### <span data-ttu-id="72039-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="72039-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="72039-113">A "ConstosoApp" nevű webalkalmazás pillanatfelvételének beszerzése a "Default-Web-WestUS" erőforráscsoporthoz tartozó "staging" nevű bővítőhelykel</span><span class="sxs-lookup"><span data-stu-id="72039-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="72039-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="72039-114">PARAMETERS</span></span>

### <span data-ttu-id="72039-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72039-115">-DefaultProfile</span></span>
<span data-ttu-id="72039-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="72039-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72039-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="72039-117">-Name</span></span>
<span data-ttu-id="72039-118">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="72039-118">The name of the web app.</span></span>

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

### <span data-ttu-id="72039-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72039-119">-ResourceGroupName</span></span>
<span data-ttu-id="72039-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="72039-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="72039-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="72039-121">-Slot</span></span>
<span data-ttu-id="72039-122">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="72039-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="72039-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="72039-123">-WebApp</span></span>
<span data-ttu-id="72039-124">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="72039-124">The web app object</span></span>

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

## <span data-ttu-id="72039-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="72039-125">INPUTS</span></span>

### <span data-ttu-id="72039-126">System. String</span><span class="sxs-lookup"><span data-stu-id="72039-126">System.String</span></span>
<span data-ttu-id="72039-127">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="72039-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="72039-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="72039-128">OUTPUTS</span></span>

### <span data-ttu-id="72039-129">Microsoft. Azure. Command. WebApps. Parancsmags. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="72039-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="72039-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="72039-130">NOTES</span></span>

## <span data-ttu-id="72039-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="72039-131">RELATED LINKS</span></span>

