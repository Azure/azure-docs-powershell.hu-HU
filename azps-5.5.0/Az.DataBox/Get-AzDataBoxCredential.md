---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxCredential.md
ms.openlocfilehash: 308f7aa185350635815622ed684e47ebea349f9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148370"
---
# <span data-ttu-id="00d13-101">Get-AzDataBoxCredential</span><span class="sxs-lookup"><span data-stu-id="00d13-101">Get-AzDataBoxCredential</span></span>

## <span data-ttu-id="00d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00d13-102">SYNOPSIS</span></span>
<span data-ttu-id="00d13-103">Egy adott feladat adatdoboz-hitelesítő adatait kapja meg</span><span class="sxs-lookup"><span data-stu-id="00d13-103">Gets the databox credentials of a specific job</span></span>

## <span data-ttu-id="00d13-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="00d13-104">SYNTAX</span></span>

### <span data-ttu-id="00d13-105">GetByNameParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="00d13-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxCredential -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00d13-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00d13-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00d13-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="00d13-107">DESCRIPTION</span></span>
<span data-ttu-id="00d13-108">A **Get-AzDataBoxCredential** parancsmag egy adott feladat adatdobozának hitelesítő adatait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="00d13-108">The **Get-AzDataBoxCredential** cmdlet gets the credentials of the databox of a specific job.</span></span> <span data-ttu-id="00d13-109">A visszaadott hitelesítőadat-objektum belső tulajdonságai különbözőek lesznek a különböző termékváltozattípusok esetén.</span><span class="sxs-lookup"><span data-stu-id="00d13-109">The internal properties of the returned credentials object will be different for different Sku types.</span></span>

## <span data-ttu-id="00d13-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="00d13-110">EXAMPLES</span></span>

### <span data-ttu-id="00d13-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="00d13-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceGroupName TestRg1 -Name TestJob1

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="00d13-112">Ezzel a megadott feladat JobSecrets-ét adja vissza</span><span class="sxs-lookup"><span data-stu-id="00d13-112">This retuns the JobSecrets of the specified job</span></span>

### <span data-ttu-id="00d13-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="00d13-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxCredential -ResourceId "/subscriptions/fa68082f-8ff7-4a25-95c7-ce9da541242f/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/TestJob1"

JobName     JobSecrets
-------     ----------
TestJob1    Microsoft.Azure.Management.DataBox.Models.DataboxJobSecrets
```

<span data-ttu-id="00d13-114">Ezzel a megadott feladat JobSecrets-ét adja vissza</span><span class="sxs-lookup"><span data-stu-id="00d13-114">This retuns the JobSecrets of the specified job</span></span>

## <span data-ttu-id="00d13-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00d13-115">PARAMETERS</span></span>

### <span data-ttu-id="00d13-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d13-116">-DefaultProfile</span></span>
<span data-ttu-id="00d13-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="00d13-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00d13-118">-Name</span><span class="sxs-lookup"><span data-stu-id="00d13-118">-Name</span></span>
<span data-ttu-id="00d13-119">Databox Job Name</span><span class="sxs-lookup"><span data-stu-id="00d13-119">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d13-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00d13-120">-ResourceGroupName</span></span>
<span data-ttu-id="00d13-121">Databox Job Resource Group Name</span><span class="sxs-lookup"><span data-stu-id="00d13-121">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d13-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00d13-122">-ResourceId</span></span>
<span data-ttu-id="00d13-123">Databox Job Resource Id</span><span class="sxs-lookup"><span data-stu-id="00d13-123">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00d13-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d13-124">CommonParameters</span></span>
<span data-ttu-id="00d13-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d13-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d13-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00d13-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d13-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00d13-127">INPUTS</span></span>

### <span data-ttu-id="00d13-128">System.String</span><span class="sxs-lookup"><span data-stu-id="00d13-128">System.String</span></span>

## <span data-ttu-id="00d13-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="00d13-129">OUTPUTS</span></span>

### <span data-ttu-id="00d13-130">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="00d13-130">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Management.DataBox.Models.UnencryptedCredentials, Microsoft.Azure.Management.DataBox, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="00d13-131">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="00d13-131">NOTES</span></span>

## <span data-ttu-id="00d13-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="00d13-132">RELATED LINKS</span></span>
