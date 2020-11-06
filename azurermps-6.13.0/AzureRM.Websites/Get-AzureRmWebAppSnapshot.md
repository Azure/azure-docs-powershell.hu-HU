---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSnapshot.md
ms.openlocfilehash: 292364ae6355c640ed66116c84289fe303acdd53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93491821"
---
# <span data-ttu-id="b7c03-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b7c03-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="b7c03-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b7c03-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c03-103">Elérhetővé válik a webes alkalmazások számára elérhető Pillanatképek.</span><span class="sxs-lookup"><span data-stu-id="b7c03-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7c03-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b7c03-104">SYNTAX</span></span>

### <span data-ttu-id="b7c03-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b7c03-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7c03-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b7c03-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7c03-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="b7c03-107">DESCRIPTION</span></span>
<span data-ttu-id="b7c03-108">A **Get-AzureRmWebAppSnapshot** parancsmag minden pillanatképet visszaadott egy webalkalmazáshoz.</span><span class="sxs-lookup"><span data-stu-id="b7c03-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="b7c03-109">A pillanatképek automatikusan biztonsági másolatot készítenek egy webalkalmazás fájljairól és beállításairól.</span><span class="sxs-lookup"><span data-stu-id="b7c03-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="b7c03-110">Egy pillanatkép visszaállítható a **Restore-AzureRmWebAppSnapshot** parancsmaggal.</span><span class="sxs-lookup"><span data-stu-id="b7c03-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="b7c03-111">Példák</span><span class="sxs-lookup"><span data-stu-id="b7c03-111">EXAMPLES</span></span>

### <span data-ttu-id="b7c03-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="b7c03-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="b7c03-113">A "ConstosoApp" nevű webalkalmazás pillanatfelvételének beszerzése a "Default-Web-WestUS" erőforráscsoporthoz tartozó "staging" nevű bővítőhelykel</span><span class="sxs-lookup"><span data-stu-id="b7c03-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="b7c03-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b7c03-114">PARAMETERS</span></span>

### <span data-ttu-id="b7c03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c03-115">-DefaultProfile</span></span>
<span data-ttu-id="b7c03-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7c03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7c03-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="b7c03-117">-Name</span></span>
<span data-ttu-id="b7c03-118">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="b7c03-118">The name of the web app.</span></span>

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

### <span data-ttu-id="b7c03-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c03-119">-ResourceGroupName</span></span>
<span data-ttu-id="b7c03-120">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="b7c03-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7c03-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="b7c03-121">-Slot</span></span>
<span data-ttu-id="b7c03-122">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="b7c03-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="b7c03-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="b7c03-123">-WebApp</span></span>
<span data-ttu-id="b7c03-124">A Web App-objektum</span><span class="sxs-lookup"><span data-stu-id="b7c03-124">The web app object</span></span>

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

### <span data-ttu-id="b7c03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c03-125">CommonParameters</span></span>
<span data-ttu-id="b7c03-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b7c03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c03-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c03-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c03-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7c03-128">INPUTS</span></span>

### <span data-ttu-id="b7c03-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c03-129">System.String</span></span>

### <span data-ttu-id="b7c03-130">Microsoft. Azure. Management. WebSites. models. site</span><span class="sxs-lookup"><span data-stu-id="b7c03-130">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="b7c03-131">Paraméterek: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b7c03-131">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="b7c03-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7c03-132">OUTPUTS</span></span>

### <span data-ttu-id="b7c03-133">Microsoft. Azure. Command. WebApps. Parancsmags. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="b7c03-133">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="b7c03-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b7c03-134">NOTES</span></span>

## <span data-ttu-id="b7c03-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7c03-135">RELATED LINKS</span></span>
