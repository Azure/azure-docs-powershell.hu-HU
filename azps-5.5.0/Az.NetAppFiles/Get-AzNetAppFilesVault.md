---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: 9779db097028710aa8aeddc7a5a1c5bdea85a30a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207078"
---
# <span data-ttu-id="c2db4-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="c2db4-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="c2db4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2db4-102">SYNOPSIS</span></span>
<span data-ttu-id="c2db4-103">Az Azure NetApp-fájlok (ANF)-fiókok biztonsági mentési tárolóinak listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c2db4-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="c2db4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c2db4-104">SYNTAX</span></span>

### <span data-ttu-id="c2db4-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c2db4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2db4-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2db4-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2db4-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2db4-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2db4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c2db4-108">DESCRIPTION</span></span>
<span data-ttu-id="c2db4-109">A **Get-AzNetAppFilesVault parancsmag** egy ANF-fiókok biztonságimásolat-tárolóit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c2db4-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="c2db4-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c2db4-110">EXAMPLES</span></span>

### <span data-ttu-id="c2db4-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c2db4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="c2db4-112">Ez a parancs lekérte az Azure NetappFiles (ANF) fiók "MyAnfAccount" biztonsági mentési tárolóit.</span><span class="sxs-lookup"><span data-stu-id="c2db4-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="c2db4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2db4-113">PARAMETERS</span></span>

### <span data-ttu-id="c2db4-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2db4-114">-AccountName</span></span>
<span data-ttu-id="c2db4-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="c2db4-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2db4-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="c2db4-116">-AccountObject</span></span>
<span data-ttu-id="c2db4-117">Az új biztonságimásolat-objektum fiókja</span><span class="sxs-lookup"><span data-stu-id="c2db4-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="c2db4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2db4-118">-DefaultProfile</span></span>
<span data-ttu-id="c2db4-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2db4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2db4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2db4-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2db4-121">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="c2db4-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="c2db4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2db4-122">-ResourceId</span></span>
<span data-ttu-id="c2db4-123">Az ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="c2db4-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="c2db4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2db4-124">CommonParameters</span></span>
<span data-ttu-id="c2db4-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2db4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2db4-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2db4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2db4-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2db4-127">INPUTS</span></span>

### <span data-ttu-id="c2db4-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="c2db4-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="c2db4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c2db4-129">System.String</span></span>

## <span data-ttu-id="c2db4-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2db4-130">OUTPUTS</span></span>

### <span data-ttu-id="c2db4-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="c2db4-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="c2db4-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c2db4-132">NOTES</span></span>

## <span data-ttu-id="c2db4-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2db4-133">RELATED LINKS</span></span>
