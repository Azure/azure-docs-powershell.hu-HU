---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845354"
---
# <span data-ttu-id="5ca29-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5ca29-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="5ca29-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ca29-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca29-103">Automatizálási hitelesítő adatok módosítása</span><span class="sxs-lookup"><span data-stu-id="5ca29-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="5ca29-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ca29-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ca29-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ca29-105">DESCRIPTION</span></span>
<span data-ttu-id="5ca29-106">A **set-AzAutomationCredential** parancsmag **PSCredential** -objektumként módosítja a hitelesítő adatokat az Azure automatizálásban.</span><span class="sxs-lookup"><span data-stu-id="5ca29-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="5ca29-107">Példák</span><span class="sxs-lookup"><span data-stu-id="5ca29-107">EXAMPLES</span></span>

### <span data-ttu-id="5ca29-108">Példa 1: hitelesítő adatok frissítése</span><span class="sxs-lookup"><span data-stu-id="5ca29-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="5ca29-109">Az első parancs a felhasználónevet hozzárendeli a $User változóhoz.</span><span class="sxs-lookup"><span data-stu-id="5ca29-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="5ca29-110">A második parancs az egyszerű szöveges jelszót egy biztonságos karakterláncba konvertálja a ConvertTo-SecureString parancsmag használatával.</span><span class="sxs-lookup"><span data-stu-id="5ca29-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="5ca29-111">A parancs az objektumot a $Password változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca29-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="5ca29-112">A harmadik parancs a hitelesítő adatokat $User és a $Password alapján hozza létre, majd a $Credential változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="5ca29-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="5ca29-113">A végleges parancs módosítja a ContosoCredential nevű automatizálási hitelesítő adatokat, hogy a hitelesítő adatokat használja a $Credentialban.</span><span class="sxs-lookup"><span data-stu-id="5ca29-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="5ca29-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ca29-114">PARAMETERS</span></span>

### <span data-ttu-id="5ca29-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5ca29-115">-AutomationAccountName</span></span>
<span data-ttu-id="5ca29-116">Annak az automatizálási fióknak a nevét adja meg, amelyhez ez a parancsmag módosítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="5ca29-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca29-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca29-117">-DefaultProfile</span></span>
<span data-ttu-id="5ca29-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="5ca29-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ca29-119">-Leírás</span><span class="sxs-lookup"><span data-stu-id="5ca29-119">-Description</span></span>
<span data-ttu-id="5ca29-120">A parancsmag által módosított hitelesítő adatok leírását adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ca29-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca29-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ca29-121">-Name</span></span>
<span data-ttu-id="5ca29-122">Annak a hitelesítő adatoknak a neve, amelyet a parancsmag módosított.</span><span class="sxs-lookup"><span data-stu-id="5ca29-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca29-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca29-123">-ResourceGroupName</span></span>
<span data-ttu-id="5ca29-124">Annak az erőforráscsoport-csoportnak a nevét adja meg, amelyhez ez a parancsmag módosítja a hitelesítő adatokat.</span><span class="sxs-lookup"><span data-stu-id="5ca29-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca29-125">-Value (érték)</span><span class="sxs-lookup"><span data-stu-id="5ca29-125">-Value</span></span>
<span data-ttu-id="5ca29-126">A hitelesítő adatokat **PSCredential** -objektumként adja meg.</span><span class="sxs-lookup"><span data-stu-id="5ca29-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca29-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca29-127">CommonParameters</span></span>
<span data-ttu-id="5ca29-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ca29-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca29-129">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ca29-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca29-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca29-130">INPUTS</span></span>

### <span data-ttu-id="5ca29-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5ca29-131">System.String</span></span>

### <span data-ttu-id="5ca29-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="5ca29-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="5ca29-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ca29-133">OUTPUTS</span></span>

### <span data-ttu-id="5ca29-134">Microsoft. Azure. Command. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="5ca29-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="5ca29-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ca29-135">NOTES</span></span>

## <span data-ttu-id="5ca29-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ca29-136">RELATED LINKS</span></span>

[<span data-ttu-id="5ca29-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5ca29-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="5ca29-138">Új – AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5ca29-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="5ca29-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5ca29-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


