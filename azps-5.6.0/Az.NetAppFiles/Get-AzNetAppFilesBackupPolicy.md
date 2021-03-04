---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesbackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackupPolicy.md
ms.openlocfilehash: fc8e3d49f5c5a6430a6436b0d46e8fd10984db98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926929"
---
# <span data-ttu-id="b5d36-101">Get-AzNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b5d36-101">Get-AzNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b5d36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5d36-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d36-103">Részleteket kap az Azure NetApp-fájlok biztonsági mentésére vonatkozó házirendről.</span><span class="sxs-lookup"><span data-stu-id="b5d36-103">Gets details of an Azure NetApp Files (ANF) Backup Policy.</span></span>

## <span data-ttu-id="b5d36-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="b5d36-104">SYNTAX</span></span>

### <span data-ttu-id="b5d36-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="b5d36-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackupPolicy -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5d36-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5d36-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5d36-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5d36-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackupPolicy [-Name <String>] -AccountObject <PSNetAppFilesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5d36-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="b5d36-108">DESCRIPTION</span></span>
<span data-ttu-id="b5d36-109">A **Get-AzNetAppFilesBackupPolicy** parancsmag részletes információkat kap az ANF biztonsági mentési házirendről.</span><span class="sxs-lookup"><span data-stu-id="b5d36-109">The **Get-AzNetAppFilesBackupPolicy** cmdlet gets details of an ANF backup policy.</span></span>

## <span data-ttu-id="b5d36-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="b5d36-110">EXAMPLES</span></span>

### <span data-ttu-id="b5d36-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="b5d36-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackupPolicy -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyBackupPolicy"
```

<span data-ttu-id="b5d36-112">Ez a parancs a "MyAnfAccount" fiók "MyBackupPolicy" nevű biztonságimásolat-házirendet kapja meg.</span><span class="sxs-lookup"><span data-stu-id="b5d36-112">This command gets the backup policy named "MyBackupPolicy" for account "MyAnfAccount".</span></span>

## <span data-ttu-id="b5d36-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5d36-113">PARAMETERS</span></span>

### <span data-ttu-id="b5d36-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b5d36-114">-AccountName</span></span>
<span data-ttu-id="b5d36-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="b5d36-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="b5d36-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="b5d36-116">-AccountObject</span></span>
<span data-ttu-id="b5d36-117">The Account object containing the Backup Policy to return</span><span class="sxs-lookup"><span data-stu-id="b5d36-117">The Account object containing the Backup Policy to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5d36-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d36-118">-DefaultProfile</span></span>
<span data-ttu-id="b5d36-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b5d36-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5d36-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b5d36-120">-Name</span></span>
<span data-ttu-id="b5d36-121">Az ANF biztonsági mentési házirend neve</span><span class="sxs-lookup"><span data-stu-id="b5d36-121">The name of the ANF backup policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5d36-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5d36-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5d36-123">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="b5d36-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="b5d36-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5d36-124">-ResourceId</span></span>
<span data-ttu-id="b5d36-125">Az ANF biztonsági mentési házirend erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="b5d36-125">The resource id of the ANF Backup Policy</span></span>

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

### <span data-ttu-id="b5d36-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d36-126">CommonParameters</span></span>
<span data-ttu-id="b5d36-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5d36-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d36-128">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5d36-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d36-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5d36-129">INPUTS</span></span>

### <span data-ttu-id="b5d36-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b5d36-130">System.String</span></span>

### <span data-ttu-id="b5d36-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="b5d36-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="b5d36-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b5d36-132">OUTPUTS</span></span>

### <span data-ttu-id="b5d36-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b5d36-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="b5d36-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="b5d36-134">NOTES</span></span>

## <span data-ttu-id="b5d36-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b5d36-135">RELATED LINKS</span></span>
