---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: a67e48cdcad9d80d244e74ef8e20f81fcbd157cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934561"
---
# <span data-ttu-id="e6da5-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e6da5-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="e6da5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6da5-102">SYNOPSIS</span></span>
<span data-ttu-id="e6da5-103">Törlődnek a webalkalmazások az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="e6da5-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="e6da5-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="e6da5-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6da5-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="e6da5-105">DESCRIPTION</span></span>
<span data-ttu-id="e6da5-106">A **Get-AzDeletedWebApp** parancsmag az előfizetés összes törölt webappját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="e6da5-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="e6da5-107">A törölt appok tetszés szerint szűrhetők erőforráscsoport, név és slot szerint.</span><span class="sxs-lookup"><span data-stu-id="e6da5-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="e6da5-108">Több törölt app is lehet ugyanazokkal a névvel és erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="e6da5-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="e6da5-109">Az azonos nevű törölt appok megkülönböztetésére jelölje be a DeletionTime jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="e6da5-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="e6da5-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="e6da5-110">EXAMPLES</span></span>

### <span data-ttu-id="e6da5-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="e6da5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="e6da5-112">Ez a parancs a ContosoSite nevű törölt appokat a Default-Web-WestUS erőforráscsoporthoz tartozóként kapja meg.</span><span class="sxs-lookup"><span data-stu-id="e6da5-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e6da5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6da5-113">PARAMETERS</span></span>

### <span data-ttu-id="e6da5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6da5-114">-DefaultProfile</span></span>
<span data-ttu-id="e6da5-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="e6da5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6da5-116">-Location</span><span class="sxs-lookup"><span data-stu-id="e6da5-116">-Location</span></span>
<span data-ttu-id="e6da5-117">A törölt alkalmazás helye.</span><span class="sxs-lookup"><span data-stu-id="e6da5-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="e6da5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e6da5-118">-Name</span></span>
<span data-ttu-id="e6da5-119">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="e6da5-119">The name of the web app.</span></span>

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

### <span data-ttu-id="e6da5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6da5-120">-ResourceGroupName</span></span>
<span data-ttu-id="e6da5-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="e6da5-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="e6da5-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="e6da5-122">-Slot</span></span>
<span data-ttu-id="e6da5-123">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="e6da5-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="e6da5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6da5-124">CommonParameters</span></span>
<span data-ttu-id="e6da5-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6da5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6da5-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6da5-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6da5-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6da5-127">INPUTS</span></span>

### <span data-ttu-id="e6da5-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="e6da5-128">None</span></span>

## <span data-ttu-id="e6da5-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e6da5-129">OUTPUTS</span></span>

### <span data-ttu-id="e6da5-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e6da5-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="e6da5-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="e6da5-131">NOTES</span></span>

## <span data-ttu-id="e6da5-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e6da5-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6da5-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="e6da5-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)