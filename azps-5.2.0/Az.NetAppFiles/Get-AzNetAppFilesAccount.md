---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: 677382133dffc7e64c86d02e984f35b8572a4598
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360134"
---
# <span data-ttu-id="b7d3c-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b7d3c-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="b7d3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7d3c-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d3c-103">Az Azure NetApp-fájlok (ANF)-fiókok részleteinek lekérte.</span><span class="sxs-lookup"><span data-stu-id="b7d3c-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="b7d3c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b7d3c-104">SYNTAX</span></span>

### <span data-ttu-id="b7d3c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b7d3c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7d3c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7d3c-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7d3c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b7d3c-107">DESCRIPTION</span></span>
<span data-ttu-id="b7d3c-108">A **Get-AzNetAppFilesAccount** parancsmag anF-fiók adatait tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="b7d3c-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="b7d3c-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b7d3c-109">EXAMPLES</span></span>

### <span data-ttu-id="b7d3c-110">1. példa: ANF-fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="b7d3c-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="b7d3c-111">Ez a parancs a MyAnfAccount nevű fiókot kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b7d3c-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="b7d3c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7d3c-112">PARAMETERS</span></span>

### <span data-ttu-id="b7d3c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d3c-113">-DefaultProfile</span></span>
<span data-ttu-id="b7d3c-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b7d3c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7d3c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b7d3c-115">-Name</span></span>
<span data-ttu-id="b7d3c-116">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="b7d3c-116">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d3c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d3c-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7d3c-118">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="b7d3c-118">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7d3c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7d3c-119">-ResourceId</span></span>
<span data-ttu-id="b7d3c-120">Az ANF-fiók erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b7d3c-120">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d3c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d3c-121">CommonParameters</span></span>
<span data-ttu-id="b7d3c-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d3c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d3c-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7d3c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d3c-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7d3c-124">INPUTS</span></span>

### <span data-ttu-id="b7d3c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b7d3c-125">System.String</span></span>

## <span data-ttu-id="b7d3c-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b7d3c-126">OUTPUTS</span></span>

### <span data-ttu-id="b7d3c-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b7d3c-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="b7d3c-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b7d3c-128">NOTES</span></span>

## <span data-ttu-id="b7d3c-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b7d3c-129">RELATED LINKS</span></span>
