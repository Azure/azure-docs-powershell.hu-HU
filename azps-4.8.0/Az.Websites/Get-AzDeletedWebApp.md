---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183131"
---
# <span data-ttu-id="1e8f6-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e8f6-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="1e8f6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1e8f6-102">SYNOPSIS</span></span>
<span data-ttu-id="1e8f6-103">Törölt webalkalmazásokat kap az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="1e8f6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1e8f6-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e8f6-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="1e8f6-105">DESCRIPTION</span></span>
<span data-ttu-id="1e8f6-106">A **Get-AzDeletedWebApp** parancsmag az előfizetésben szereplő összes törölt webalkalmazást visszaállítja.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="1e8f6-107">A törölt alkalmazások tetszés szerint szűrhetők az erőforráscsoport, a név és a bővítőhely csoportban.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="1e8f6-108">Ugyanaz a név és az erőforráscsoport több törölt alkalmazást is tartalmazhat.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="1e8f6-109">Ellenőrizze a DeletionTime, hogy megkülönböztesse-e az azonos nevű törölt alkalmazásokat.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="1e8f6-110">Példák</span><span class="sxs-lookup"><span data-stu-id="1e8f6-110">EXAMPLES</span></span>

### <span data-ttu-id="1e8f6-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="1e8f6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1e8f6-112">Ez a parancs beolvassa a ContosoSite nevű törölt alkalmazásokat az erőforráscsoport alapértelmezett – web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1e8f6-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1e8f6-113">PARAMETERS</span></span>

### <span data-ttu-id="1e8f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e8f6-114">-DefaultProfile</span></span>
<span data-ttu-id="1e8f6-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e8f6-116">-Hely</span><span class="sxs-lookup"><span data-stu-id="1e8f6-116">-Location</span></span>
<span data-ttu-id="1e8f6-117">A törölt alkalmazás helye.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-117">The location of the deleted app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e8f6-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1e8f6-118">-Name</span></span>
<span data-ttu-id="1e8f6-119">A Web App neve.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-119">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e8f6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e8f6-120">-ResourceGroupName</span></span>
<span data-ttu-id="1e8f6-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e8f6-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="1e8f6-122">-Slot</span></span>
<span data-ttu-id="1e8f6-123">A Web App-bővítőhely neve.</span><span class="sxs-lookup"><span data-stu-id="1e8f6-123">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e8f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e8f6-124">CommonParameters</span></span>
<span data-ttu-id="1e8f6-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1e8f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e8f6-126">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e8f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e8f6-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e8f6-127">INPUTS</span></span>

### <span data-ttu-id="1e8f6-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="1e8f6-128">None</span></span>

## <span data-ttu-id="1e8f6-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1e8f6-129">OUTPUTS</span></span>

### <span data-ttu-id="1e8f6-130">Microsoft. Azure. Command. WebApps. Parancsmags. WebApps. PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e8f6-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="1e8f6-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1e8f6-131">NOTES</span></span>

## <span data-ttu-id="1e8f6-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1e8f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="1e8f6-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="1e8f6-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)