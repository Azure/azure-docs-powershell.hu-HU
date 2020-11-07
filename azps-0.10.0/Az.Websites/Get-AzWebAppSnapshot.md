---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842769"
---
# <span data-ttu-id="167e5-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="167e5-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="167e5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="167e5-102">SYNOPSIS</span></span>
<span data-ttu-id="167e5-103">Elérhetővé válik a webes alkalmazások számára elérhető Pillanatképek.</span><span class="sxs-lookup"><span data-stu-id="167e5-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="167e5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="167e5-104">SYNTAX</span></span>

### <span data-ttu-id="167e5-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="167e5-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="167e5-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="167e5-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="167e5-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="167e5-107">DESCRIPTION</span></span>
<span data-ttu-id="167e5-108">A **Get-AzWebAppSnapshot** parancsmag minden pillanatképet visszaadott egy webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="167e5-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="167e5-109">A pillanatképek automatikusan biztonsági másolatot készítenek egy webalkalmazás fájljairól és beállításairól.</span><span class="sxs-lookup"><span data-stu-id="167e5-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="167e5-110">Egy pillanatkép visszaállítható a **Restore-AzWebAppSnapshot** parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="167e5-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="167e5-111">Példák</span><span class="sxs-lookup"><span data-stu-id="167e5-111">EXAMPLES</span></span>

### <span data-ttu-id="167e5-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="167e5-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="167e5-113">A "ConstosoApp" nevű webalkalmazás pillanatfelvételének beszerzése a "Default-Web-WestUS" erőforráscsoporthoz tartozó "staging" nevű bővítőhelykel</span><span class="sxs-lookup"><span data-stu-id="167e5-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="167e5-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="167e5-114">PARAMETERS</span></span>

### <span data-ttu-id="167e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="167e5-115">-DefaultProfile</span></span>
<span data-ttu-id="167e5-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="167e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="167e5-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="167e5-117">-Name</span></span>
<span data-ttu-id="167e5-118">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="167e5-118">The name of the web app.</span></span>

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

### <span data-ttu-id="167e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="167e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="167e5-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="167e5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="167e5-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="167e5-121">-Slot</span></span>
<span data-ttu-id="167e5-122">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="167e5-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="167e5-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="167e5-123">-WebApp</span></span>
<span data-ttu-id="167e5-124">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="167e5-124">The web app object</span></span>

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

## <span data-ttu-id="167e5-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="167e5-125">INPUTS</span></span>

### <span data-ttu-id="167e5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="167e5-126">System.String</span></span>
<span data-ttu-id="167e5-127">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="167e5-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="167e5-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="167e5-128">OUTPUTS</span></span>

### <span data-ttu-id="167e5-129">Microsoft. Azure. Command. WebApps. Parancsmags. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="167e5-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="167e5-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="167e5-130">NOTES</span></span>

## <span data-ttu-id="167e5-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="167e5-131">RELATED LINKS</span></span>

