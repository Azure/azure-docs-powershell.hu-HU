---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVault.md
ms.openlocfilehash: d2741b3eb10618b9bdbe2e97b14d176c2b3eab26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926889"
---
# <span data-ttu-id="02ec9-101">Get-AzNetAppFilesVault</span><span class="sxs-lookup"><span data-stu-id="02ec9-101">Get-AzNetAppFilesVault</span></span>

## <span data-ttu-id="02ec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="02ec9-103">Az Azure NetApp-fájlok (ANF)-fiókok biztonsági mentési tárolóinak listáját tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="02ec9-103">Gets list of Azure NetApp Files (ANF) Accounts backup vaults.</span></span>

## <span data-ttu-id="02ec9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="02ec9-104">SYNTAX</span></span>

### <span data-ttu-id="02ec9-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="02ec9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVault -ResourceGroupName <String> [-AccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="02ec9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ec9-106">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVault -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="02ec9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ec9-107">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVault -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02ec9-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="02ec9-108">DESCRIPTION</span></span>
<span data-ttu-id="02ec9-109">A **Get-AzNetAppFilesVault parancsmag** egy ANF-fiókok biztonságimásolat-tárolóit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="02ec9-109">The **Get-AzNetAppFilesVault** cmdlet gets list of an ANF accounts backup vaults.</span></span>

## <span data-ttu-id="02ec9-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="02ec9-110">EXAMPLES</span></span>

### <span data-ttu-id="02ec9-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="02ec9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesVault -ResourceGroupName "MyRG" -AccountName "MyAnfAccount"
```

<span data-ttu-id="02ec9-112">Ez a parancs lekérte az Azure NetappFiles (ANF) fiók "MyAnfAccount" biztonsági mentési tárolóit.</span><span class="sxs-lookup"><span data-stu-id="02ec9-112">This command gets a list of the backup vaults for Azure NetappFiles (ANF) account "MyAnfAccount".</span></span>

## <span data-ttu-id="02ec9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02ec9-113">PARAMETERS</span></span>

### <span data-ttu-id="02ec9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02ec9-114">-AccountName</span></span>
<span data-ttu-id="02ec9-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="02ec9-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="02ec9-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="02ec9-116">-AccountObject</span></span>
<span data-ttu-id="02ec9-117">Az új biztonságimásolat-objektum fiókja</span><span class="sxs-lookup"><span data-stu-id="02ec9-117">The account for the new backup object</span></span>

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

### <span data-ttu-id="02ec9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ec9-118">-DefaultProfile</span></span>
<span data-ttu-id="02ec9-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="02ec9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ec9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ec9-120">-ResourceGroupName</span></span>
<span data-ttu-id="02ec9-121">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="02ec9-121">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="02ec9-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02ec9-122">-ResourceId</span></span>
<span data-ttu-id="02ec9-123">Az ANF-készlet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="02ec9-123">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="02ec9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ec9-124">CommonParameters</span></span>
<span data-ttu-id="02ec9-125">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ec9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ec9-126">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02ec9-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ec9-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02ec9-127">INPUTS</span></span>

### <span data-ttu-id="02ec9-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="02ec9-128">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

### <span data-ttu-id="02ec9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="02ec9-129">System.String</span></span>

## <span data-ttu-id="02ec9-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="02ec9-130">OUTPUTS</span></span>

### <span data-ttu-id="02ec9-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="02ec9-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackupPolicy</span></span>

## <span data-ttu-id="02ec9-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="02ec9-132">NOTES</span></span>

## <span data-ttu-id="02ec9-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="02ec9-133">RELATED LINKS</span></span>
