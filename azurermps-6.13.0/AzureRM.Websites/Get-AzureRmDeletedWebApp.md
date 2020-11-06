---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmDeletedWebApp.md
ms.openlocfilehash: 75ad4e1fabb511ee4ca3cff024389a8e826aeadd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497183"
---
# <span data-ttu-id="e67d7-101">Get-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e67d7-101">Get-AzureRmDeletedWebApp</span></span>

## <span data-ttu-id="e67d7-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e67d7-102">SYNOPSIS</span></span>
<span data-ttu-id="e67d7-103">Törölt webalkalmazásokat kap az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="e67d7-103">Gets deleted web apps in the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e67d7-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e67d7-104">SYNTAX</span></span>

```
Get-AzureRmDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e67d7-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e67d7-105">DESCRIPTION</span></span>
<span data-ttu-id="e67d7-106">A **Get-AzureRmDeletedWebApp** parancsmag az előfizetésben szereplő összes törölt webalkalmazást visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="e67d7-106">The **Get-AzureRmDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="e67d7-107">A törölt alkalmazások tetszés szerint szűrhetők az erőforráscsoport, a név és a bővítőhely csoportban.</span><span class="sxs-lookup"><span data-stu-id="e67d7-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="e67d7-108">Ugyanaz a név és az erőforráscsoport több törölt alkalmazást is tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="e67d7-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="e67d7-109">Ellenőrizze a DeletionTime, hogy megkülönböztesse-e az azonos nevű törölt alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="e67d7-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="e67d7-110">Példák</span><span class="sxs-lookup"><span data-stu-id="e67d7-110">EXAMPLES</span></span>

### <span data-ttu-id="e67d7-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="e67d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e67d7-112">Ez a parancs beolvassa a ContosoSite nevű törölt alkalmazásokat az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="e67d7-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e67d7-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e67d7-113">PARAMETERS</span></span>

### <span data-ttu-id="e67d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67d7-114">-DefaultProfile</span></span>
<span data-ttu-id="e67d7-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e67d7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e67d7-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="e67d7-116">-Name</span></span>
<span data-ttu-id="e67d7-117">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="e67d7-117">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67d7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e67d7-118">-ResourceGroupName</span></span>
<span data-ttu-id="e67d7-119">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e67d7-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67d7-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="e67d7-120">-Slot</span></span>
<span data-ttu-id="e67d7-121">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="e67d7-121">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67d7-122">CommonParameters</span></span>
<span data-ttu-id="e67d7-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e67d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e67d7-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e67d7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67d7-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e67d7-125">INPUTS</span></span>

### <span data-ttu-id="e67d7-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="e67d7-126">None</span></span>

## <span data-ttu-id="e67d7-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e67d7-127">OUTPUTS</span></span>

### <span data-ttu-id="e67d7-128">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e67d7-128">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="e67d7-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e67d7-129">NOTES</span></span>

## <span data-ttu-id="e67d7-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e67d7-130">RELATED LINKS</span></span>

[<span data-ttu-id="e67d7-131">Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e67d7-131">Restore-AzureRmDeletedWebApp</span></span>](./Restore-AzureRmDeletedWebApp.md)
