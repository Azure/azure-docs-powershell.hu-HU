---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azdeletedwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzDeletedWebApp.md
ms.openlocfilehash: 74c518d4713c19c7a1bb7b7d0b3341e164e22c35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149714"
---
# <span data-ttu-id="93f6c-101">Get-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="93f6c-101">Get-AzDeletedWebApp</span></span>

## <span data-ttu-id="93f6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f6c-102">SYNOPSIS</span></span>
<span data-ttu-id="93f6c-103">Törlődnek a webalkalmazások az előfizetésből.</span><span class="sxs-lookup"><span data-stu-id="93f6c-103">Gets deleted web apps in the subscription.</span></span>

## <span data-ttu-id="93f6c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93f6c-104">SYNTAX</span></span>

```
Get-AzDeletedWebApp [[-ResourceGroupName] <String>] [[-Name] <String>] [[-Slot] <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93f6c-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93f6c-105">DESCRIPTION</span></span>
<span data-ttu-id="93f6c-106">A **Get-AzDeletedWebApp** parancsmag az előfizetés összes törölt webappját visszaadja.</span><span class="sxs-lookup"><span data-stu-id="93f6c-106">The **Get-AzDeletedWebApp** cmdlet returns all deleted web apps in the subscription.</span></span> <span data-ttu-id="93f6c-107">A törölt appok tetszés szerint szűrhetők erőforráscsoport, név és slot szerint.</span><span class="sxs-lookup"><span data-stu-id="93f6c-107">Deleted apps can optionally be filtered by resource group, name, and slot.</span></span> <span data-ttu-id="93f6c-108">Több törölt app is lehet ugyanazokkal a névvel és erőforráscsoporttal.</span><span class="sxs-lookup"><span data-stu-id="93f6c-108">There can be more than one deleted app with the same name and resource group.</span></span> <span data-ttu-id="93f6c-109">Az azonos nevű törölt appok megkülönböztetésére jelölje be a DeletionTime jelölőnégyzetet.</span><span class="sxs-lookup"><span data-stu-id="93f6c-109">Check the DeletionTime to distinguish deleted apps that share the same name.</span></span>

## <span data-ttu-id="93f6c-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93f6c-110">EXAMPLES</span></span>

### <span data-ttu-id="93f6c-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="93f6c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeletedWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="93f6c-112">Ez a parancs a ContosoSite nevű törölt appokat a Default-Web-WestUS erőforráscsoporthoz tartozóként kapja meg.</span><span class="sxs-lookup"><span data-stu-id="93f6c-112">This command gets the deleted apps named ContosoSite belonging to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="93f6c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93f6c-113">PARAMETERS</span></span>

### <span data-ttu-id="93f6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f6c-114">-DefaultProfile</span></span>
<span data-ttu-id="93f6c-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="93f6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93f6c-116">-Location</span><span class="sxs-lookup"><span data-stu-id="93f6c-116">-Location</span></span>
<span data-ttu-id="93f6c-117">A törölt alkalmazás helye.</span><span class="sxs-lookup"><span data-stu-id="93f6c-117">The location of the deleted app.</span></span>

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

### <span data-ttu-id="93f6c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="93f6c-118">-Name</span></span>
<span data-ttu-id="93f6c-119">A webalkalmazás neve.</span><span class="sxs-lookup"><span data-stu-id="93f6c-119">The name of the web app.</span></span>

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

### <span data-ttu-id="93f6c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f6c-120">-ResourceGroupName</span></span>
<span data-ttu-id="93f6c-121">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="93f6c-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="93f6c-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="93f6c-122">-Slot</span></span>
<span data-ttu-id="93f6c-123">A webalkalmazás-slot neve.</span><span class="sxs-lookup"><span data-stu-id="93f6c-123">The name of the web app slot.</span></span>

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

### <span data-ttu-id="93f6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f6c-124">CommonParameters</span></span>
<span data-ttu-id="93f6c-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f6c-126">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f6c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f6c-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93f6c-127">INPUTS</span></span>

### <span data-ttu-id="93f6c-128">Nincs</span><span class="sxs-lookup"><span data-stu-id="93f6c-128">None</span></span>

## <span data-ttu-id="93f6c-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93f6c-129">OUTPUTS</span></span>

### <span data-ttu-id="93f6c-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="93f6c-130">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.PSAzureDeletedWebApp</span></span>

## <span data-ttu-id="93f6c-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93f6c-131">NOTES</span></span>

## <span data-ttu-id="93f6c-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93f6c-132">RELATED LINKS</span></span>

[<span data-ttu-id="93f6c-133">Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="93f6c-133">Restore-AzDeletedWebApp</span></span>](./Restore-AzDeletedWebApp.md)